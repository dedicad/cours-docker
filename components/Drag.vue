<script lang="ts">
export default {
    data(vm) {
        return {
            osiLayers: [
                '7. Application',
                '6. Présentation',
                '5. Session',
                '4. Transport',
                '3. Réseau',
                '2. Liaison de données',
                '1. Physique',
            ],
            osiElements: [
                'Fibre Optique',
                'HTML',
                'JSON',
                'NFC',
                'bluetooth',
                'Adressage Physique (MAC)',
                'Adressage Logique (IP)',
                'Protocole TCP',
                'Protocole UDP',
                'CSV',
                'SMTP',
                'POP3',
                'HTTPS',
            ],
        };
    },
    methods: {
        dragstartHandler(ev) {
            // Add the target element's id to the data transfer object
            ev.dataTransfer.setData('application/my-app', ev.target.id);
            ev.dataTransfer.effectAllowed = 'move';
        },
        dragoverHandler(ev) {
            ev.preventDefault();
            ev.dataTransfer.dropEffect = 'move';
        },
        dragEnterHandler(ev) {
            ev.target.setAttribute('style', 'border-color:#FFFFFF;');
        },
        dragexitHandler(ev) {
            ev.target.setAttribute('style', 'border-color:##3949AB;');
        },
        dropHandler(ev) {
            ev.preventDefault();
            // Get the id of the target and add the moved element to the target's DOM
            const data = ev.dataTransfer.getData('application/my-app');
            ev.target.appendChild(document.getElementById(data));
            ev.target.setAttribute('style', 'border-color:##3949AB;');
        },
    },
};
</script>

<template>
    <div class="flex flex-row justify-between">
        <div
            class="flex-column justify-between text-[12px] border-2 p-5 border-rd-lg w-70"
            @drop="dropHandler"
            @dragover="dragoverHandler"
            @dragenter="dragEnterHandler"
            @dragexit="dragexitHandler"
        >
            <div
                v-for="osiElement in osiElements"
                :key="osiElement"
                :id="osiElement"
                draggable="true"
                @dragstart="dragstartHandler"
                class="mt-2 p-0 hover:cursor-grab hover:border-gray border-2 border-transparent"
            >
                {{ osiElement }}
            </div>
        </div>
        <div class="w-150">
            <div
                v-for="layerName in osiLayers"
                :key="layerName"
                @drop="dropHandler"
                @dragover="dragoverHandler"
                @dragenter="dragEnterHandler"
                @dragexit="dragexitHandler"
                class="p-1 m-1 bg-indigo-400 border-rd-lg border-double border-2 hover:border-dotted border-indigo-600 text-[12px] flex flex-row justify-between"
            >
                {{ layerName }}:
            </div>
        </div>
    </div>
</template>

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Recipe Editor Pro - Tecnoeka Touchscreen series recipe editor</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/sql.js/1.8.0/sql-wasm.js"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    
    <style>
        body { background-color: #f8fafc; color: #334155; }
        .step-card { background: white; border: 1px solid #e2e8f0; border-radius: 28px; border-l-8 border-l-blue-600; }
        .cat-card { transition: all 0.2s ease; border: 2px solid transparent; background: #ffffff; cursor: pointer; display: flex; flex-direction: column; align-items: center; justify-content: center; text-align: center; min-height: 85px; }
        .cat-card.selected { border-color: #2563eb; background-color: #eff6ff; color: #1d4ed8; transform: translateY(-2px); }
        input[type=range] { accent-color: #2563eb; cursor: pointer; height: 8px; border-radius: 4px; }
        .accordion-content { transition: all 0.3s ease; max-height: 0; overflow: hidden; }
        .accordion-content.open { max-height: 1200px; padding-top: 1rem; }
        .info-text { font-size: 0.7rem; line-height: 1rem; color: #64748b; margin-top: 0.5rem; font-style: italic; }
        .img-preview-container { width: 205px; height: 150px; overflow: hidden; border-radius: 20px; border: 2px dashed #cbd5e1; display: flex; align-items: center; justify-content: center; background: #f1f5f9; position: relative; transition: all 0.3s; }
        .guide-box { background: linear-gradient(135deg, #eff6ff 0%, #ffffff 100%); border: 1px solid #dbeafe; }
        input:disabled { background-color: #f8fafc; color: #cbd5e1; cursor: not-allowed; border-color: #f1f5f9; }
        input::-webkit-outer-spin-button, input::-webkit-inner-spin-button { -webkit-appearance: none; margin: 0; }
    </style>
</head>
<body class="min-h-screen font-sans pb-20 text-slate-700">

    <!-- LANGUAGE SELECTOR -->
    <div class="w-full bg-white border-b border-slate-200 py-3 mb-6">
        <div class="container mx-auto px-8 flex justify-center md:justify-end gap-4">
            <div class="flex bg-slate-100 p-1 rounded-xl border border-slate-200 shadow-sm">
                <input type="radio" name="lang" id="lang_en" value="en" class="hidden lang-radio" checked onchange="changeLanguage('en')">
                <label for="lang_en" class="px-4 py-1.5 rounded-lg text-[10px] font-bold uppercase cursor-pointer transition-all flex items-center gap-2">
                    <span>🇬🇧</span> English
                </label>
                <input type="radio" name="lang" id="lang_hr" value="hr" class="hidden lang-radio" onchange="changeLanguage('hr')">
                <label for="lang_hr" class="px-4 py-1.5 rounded-lg text-[10px] font-bold uppercase cursor-pointer transition-all flex items-center gap-2">
                    <span>🇭🇷</span> Hrvatski
                </label>
                <input type="radio" name="lang" id="lang_it" value="it" class="hidden lang-radio" onchange="changeLanguage('it')">
                <label for="lang_it" class="px-4 py-1.5 rounded-lg text-[10px] font-bold uppercase cursor-pointer transition-all flex items-center gap-2">
                    <span>🇮🇹</span> Italiano
                </label>
            </div>
        </div>
    </div>

    <div class="container mx-auto p-4 md:p-8">
        
        <!-- Welcome & Info Section -->
        <div id="welcomeScreen" class="mb-10 p-8 rounded-[40px] guide-box shadow-sm w-full">
            <div class="w-full">
                <h2 class="text-3xl font-black text-slate-800 mb-4" data-i18n="appWelcome">Welcome to Recipe Editor Pro</h2>
                <p class="text-slate-600 mb-10 leading-relaxed text-lg w-full" data-i18n="appIntro">Tecnoeka touchscreen (TS) oven recipe management application.</p>
                
                <div class="grid grid-cols-1 md:grid-cols-3 gap-8 mb-12">
                    <div class="bg-white/50 p-6 rounded-3xl border border-blue-100">
                        <div class="w-10 h-10 rounded-full bg-blue-600 text-white flex items-center justify-center font-bold mb-4">1</div>
                        <h4 class="font-bold text-slate-800 mb-2 uppercase text-xs" data-i18n="step1Title">Load database</h4>
                        <p class="text-xs text-slate-500" data-i18n="step1Desc">Pick the <b>/chef</b> folder from your Tecnoeka exported recipes.</p>
                    </div>
                    <div class="bg-white/50 p-6 rounded-3xl border border-blue-100">
                        <div class="w-10 h-10 rounded-full bg-blue-600 text-white flex items-center justify-center font-bold mb-4">2</div>
                        <h4 class="font-bold text-slate-800 mb-2 uppercase text-xs" data-i18n="step2Title">Grant Access</h4>
                        <p class="text-xs text-slate-500" data-i18n="step2Desc">Accept "Edit Files" permission to automatically sync recipe changes to the recipe database.</p>
                    </div>
                    <div class="bg-white/50 p-6 rounded-3xl border border-blue-100">
                        <div class="w-10 h-10 rounded-full bg-blue-600 text-white flex items-center justify-center font-bold mb-4">3</div>
                        <h4 class="font-bold text-slate-800 mb-2 uppercase text-xs" data-i18n="step3Title">Edit & Save</h4>
                        <p class="text-xs text-slate-500" data-i18n="step3Desc">Changes to recipes are saved instantly to the recipe database.</p>
                    </div>
                </div>

                <div class="border-t border-blue-100 pt-10">
                    <h3 class="text-xl font-black text-slate-800 mb-6 uppercase" data-i18n="hardwareGuideTitle">Oven Data Exchange Guide</h3>
                    <div class="grid grid-cols-1 md:grid-cols-2 gap-10">
                        <div class="space-y-4">
                            <h5 class="font-bold text-blue-600 flex items-center gap-2"><i class="fas fa-file-export"></i> <span data-i18n="hwExportTitle">Export</span></h5>
                            <p class="text-sm text-slate-600" data-i18n="hwExportDesc"></p>
                        </div>
                        <div class="space-y-4">
                            <h5 class="font-bold text-emerald-600 flex items-center gap-2"><i class="fas fa-file-import"></i> <span data-i18n="hwImportTitle">Import</span></h5>
                            <p class="text-sm text-slate-600" data-i18n="hwImportDesc"></p>
                        </div>
                    </div>
                </div>
            </div>
        </div>

        <!-- Main Header -->
        <div class="flex flex-col md:flex-row justify-between items-center mb-10 bg-white p-6 rounded-[32px] border border-slate-200 gap-4 shadow-sm">
            <div class="flex items-center gap-5">
                <div class="bg-blue-600 p-3.5 rounded-2xl text-white shadow-lg"><i class="fas fa-database text-2xl"></i></div>
                <div>
                    <h1 class="text-xl font-black uppercase tracking-tight">Recipe editor pro</h1>
                    <p id="dbStatus" class="text-[10px] text-red-500 font-bold uppercase tracking-widest flex items-center gap-2">
                        <span class="w-2 h-2 rounded-full bg-red-500 animate-pulse"></span> <span data-i18n="disconnected">DISCONNECTED</span>
                    </p>
                </div>
            </div>

            <div class="flex flex-wrap items-center gap-3">
                <button id="initBtn" onclick="initProject()" class="bg-blue-600 hover:bg-blue-700 text-white px-6 py-2.5 rounded-xl shadow-lg transition font-bold text-xs uppercase" data-i18n="initBtn">Initialize Project</button>
                <div id="actionBtns" class="hidden flex gap-2">
                    <button onclick="openModal()" class="bg-blue-600 hover:bg-blue-700 text-white px-5 py-2.5 rounded-xl font-bold text-xs uppercase shadow-md" data-i18n="addRecipe">+ Add Recipe</button>
                    <button id="restoreBtn" onclick="restoreFromBackup()" class="bg-orange-500 hover:bg-orange-600 text-white px-5 py-2.5 rounded-xl font-bold text-xs uppercase hidden shadow-md" data-i18n="restoreBackup">Restore Backup</button>
                </div>
            </div>
        </div>

        <div id="recipeGrid" class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 xl:grid-cols-4 gap-6"></div>
    </div>

    <!-- Modal Editor -->
    <div id="modal" class="fixed inset-0 bg-slate-900/40 hidden flex items-center justify-center z-50 p-0 md:p-4 backdrop-blur-sm">
        <div class="bg-slate-50 w-full max-w-5xl h-full md:h-auto md:max-h-[95vh] overflow-y-auto md:rounded-[48px] shadow-2xl flex flex-col border border-white">
            <div class="p-8 border-b bg-white/80 backdrop-blur-md flex justify-between items-center sticky top-0 z-20">
                <h2 id="modalTitle" class="text-lg font-black uppercase tracking-widest text-slate-800" data-i18n="editorTitle">Recipe Editor</h2>
                <button onclick="closeModal()" class="w-12 h-12 flex items-center justify-center rounded-full hover:bg-slate-100 text-slate-400 hover:text-red-500 transition"><i class="fas fa-times text-xl"></i></button>
            </div>
            
            <form id="recipeForm" class="p-8 space-y-10">
                <input type="hidden" id="recipeId"><input type="hidden" id="existing_img_name">
                
                <!-- Main Info Section -->
                <div class="bg-white p-10 rounded-[40px] border border-slate-100 shadow-sm space-y-8">
                    <div class="space-y-2">
                        <label class="text-[10px] font-black uppercase text-slate-400 tracking-widest ml-1" data-i18n="recipeName">Recipe Name</label>
                        <input type="text" id="name_lang_1" required class="w-full bg-slate-50 border border-slate-200 rounded-2xl p-5 font-bold text-xl outline-none focus:border-blue-500 transition">
                    </div>
                    <div class="flex flex-col items-center py-4 border-y border-slate-50">
                        <label class="text-[10px] font-black uppercase text-slate-400 tracking-widest mb-4" data-i18n="recipeImage">Recipe Image</label>
                        <div class="img-preview-container group cursor-pointer shadow-md" onclick="document.getElementById('imgUpload').click()">
                            <img id="imgPreview" src="" alt="Preview">
                            <div class="absolute inset-0 bg-black/40 opacity-0 group-hover:opacity-100 transition flex flex-col items-center justify-center text-white p-4 text-center">
                                <i class="fas fa-camera text-2xl mb-2"></i><span class="text-[10px] font-black uppercase" data-i18n="changeImg">Change Image</span>
                            </div>
                        </div>
                        <input type="file" id="imgUpload" accept="image/*" class="hidden" onchange="processImage(this)">
                        <p class="text-[9px] text-slate-400 mt-4 text-center" data-i18n="imgNote"></p>
                    </div>
                    <div class="space-y-4">
                        <label class="text-[10px] font-black uppercase text-slate-400 tracking-widest ml-1 text-center block" data-i18n="selectCategory">Select Category</label>
                        <div id="categoryPicker" class="grid grid-cols-3 sm:grid-cols-5 md:grid-cols-9 gap-3"></div>
                        <input type="hidden" id="selected_cat_id" value="0">
                    </div>
                </div>

                <!-- Global Toggles -->
                <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
                    <div class="bg-white p-8 rounded-[32px] border-2 border-slate-100 shadow-sm">
                        <label class="flex items-center justify-between cursor-pointer group mb-4"><span class="text-xs font-black uppercase text-slate-500" data-i18n="preheat">Pre-heating</span><div class="relative"><input type="checkbox" id="preheat" class="sr-only peer"><div class="w-11 h-6 bg-slate-200 rounded-full peer peer-checked:bg-blue-600 peer-checked:after:translate-x-full after:content-[''] after:absolute after:top-[2px] after:left-[2px] after:bg-white after:rounded-full after:h-5 after:w-5 after:transition-all shadow-inner border border-slate-300"></div></div></label>
                        <p class="info-text" data-i18n="preheatDesc"></p>
                    </div>
                    <div class="bg-white p-8 rounded-[32px] border-2 border-slate-100 shadow-sm">
                        <label class="flex items-center justify-between cursor-pointer group mb-4"><span class="text-xs font-black uppercase text-slate-500" data-i18n="hold">Maintenance (Hold)</span><div class="relative"><input type="checkbox" id="hold" class="sr-only peer"><div class="w-11 h-6 bg-slate-200 rounded-full peer peer-checked:bg-orange-500 peer-checked:after:translate-x-full after:content-[''] after:absolute after:top-[2px] after:left-[2px] after:bg-white after:rounded-full after:h-5 after:w-5 after:transition-all shadow-inner border border-slate-300"></div></div></label>
                        <p class="info-text" data-i18n="holdDesc"></p>
                    </div>
                </div>

                <!-- Phases (Add Button at Top) -->
                <div class="space-y-6">
                    <div class="flex justify-between items-center px-4 border-b border-slate-100 pb-4">
                        <h3 class="text-xs font-black uppercase tracking-widest text-slate-400" data-i18n="phaseTitle">Steps (Max 4)</h3>
                        <button type="button" onclick="addPhase()" id="addPhaseBtn" class="bg-blue-600 hover:bg-blue-700 text-white text-[10px] font-black px-6 py-2.5 rounded-full shadow-lg transition uppercase tracking-widest" data-i18n="addStep">+ Add Step</button>
                    </div>
                    <div id="phasesList" class="space-y-10"></div>
                </div>

                <div class="flex gap-4 pt-8 border-t border-slate-200">
                    <button type="button" onclick="closeModal()" class="flex-1 p-5 rounded-[24px] bg-slate-200 font-bold uppercase text-xs" data-i18n="cancel">Cancel</button>
                    <button type="submit" class="flex-1 p-5 rounded-[24px] bg-blue-600 font-black uppercase text-xs text-white shadow-2xl hover:bg-blue-700 transition" data-i18n="save">Save & Sync</button>
                </div>
            </form>
        </div>
    </div>

    <script>
        const i18nData = {
            hr: {
                appWelcome: "Dobrodošli u Uređivač recepata",
                appIntro: "Jednostavna web aplikacija za upravljanje receptima na Tecnoeka (TS) pećnicama sa zaslonom osjetljivim na dodir. Dodajte, uređujte i brišite recepte s lakoćom.",
                step1Title: "Odaberite bazu podataka", step1Desc: "Odaberite lokaciju mape <b>'chef'</b> iz vaših izvezenih recepata.",
                step2Title: "Dopustite pristup", step2Desc: "Prihvatite upit internetskog preglednika za pristup i sinkronizaciju promjena izravno u bazu recepata.",
                step3Title: "Uredi i spremi", step3Desc: "Sve promjene na receptima spremaju se izravno u bazu podataka recepata.",
                hardwareGuideTitle: "Kako izvesti i uvesti recepte iz Tecnoeka pećnica",
                hwExportTitle: "Izvoz iz pećnice", hwExportDesc: "Spojite USB pogon u pećnicu. Idite na 'Postavke' - 'Uvoz/Izvoz s USB-a' i dodirnite 'Izvezi sve recepte'. Ovo će prenijeti sve recepte na USB u mapu export/recipes/chef.",
                hwImportTitle: "Uvoz u pećnicu", hwImportDesc: "Spojite USB pogon u pećnicu. Idite na 'Postavke' - 'Uvoz/Izvoz s USB-a' i dodirnite 'Uvezi sve recepte'. Recepti će biti preneseni u vašu pećnicu.",
                disconnected: "Baza recepata nije odabrana", connected: "Povezano s bazom recepata", initBtn: "Odaberite lokaciju baze podataka",
                addRecipe: "Dodaj novi recept", restoreBackup: "Vrati iz sigurnosne kopije", editorTitle: "Uređivač recepata",
                recipeName: "Naziv recepta", recipeImage: "Slika recepta", changeImg: "Promijeni sliku",
                imgNote: "Slika će biti izrezana na veličinu 205x150px.", selectCategory: "Odaberi kategoriju",
                preheat: "Predgrijavanje", hold: "Zadržavanje temperature", addStep: "Dodaj fazu", cancel: "Odustani", save: "Spremi",
                preheatDesc: "Automatski povećava temperaturu pećnice za 40°C. Kada se postigne temperatura predgrijavanja, oglasit će se zvučni signal. Nakon što otvorite i zatvorite vrata pećnice, kuhanje će započeti. Maksimalna temperatura u pećnici je 270°C.",
                holdDesc: "Održava temperaturu pećnice na 80°C u posljednjem koraku kako bi hrana ostala topla do posluživanja.",
                pulseTitle: "Semi-statični ventilator", pulseDesc: "Aktivira ventilator samo kada rade grijači. Oponaša rad statične pećnice.",
                probeEx: "Napomena: Možete definirati samo jedan temperaturni parametar za jezgrenu sondu odjednom.", probe: "Temperatura jezgrene sonde (°C)", delta: "Delta T za jezgrenu sondu (°C)",
                hours: "Sati", minutes: "Minute", temp: "Temperatura", hum: "Vlažnost", fan: "Brzina ventilatora",
                deleteConfirm: "Obrisati recept?", minTime: "Svaka faza mora trajati najmanje 1 minutu!",
                phaseTitle: "Faze (Maks. 4)", askBackup: "Izraditi sigurnosnu kopiju?",
                backupSuccess: "Sigurnosna kopija izrađena!", restorePrompt: "Odaberite datoteku sigurnosne kopije:", advancedBtn: "Napredne opcije kuhanja"
            },
            en: {
                appWelcome: "Welcome to Recipe editor pro",
                appIntro: "Simple web application for management of recipes on Tecnoeka touchscreen (TS) ovens. Add, edit and remove recipes with ease.",
                step1Title: "Select database", step1Desc: "Select the <b>'chef'</b> folder location from your exported recipes.",
                step2Title: "Allow Access", step2Desc: "Accept browser prompt to access and sync recipe changes directly to the recipe database.",
                step3Title: "Edit & Save", step3Desc: "All changes to recipes are saved directly to recipe database.",
                hardwareGuideTitle: "How to export and import recipes from Tecnoeka ovens",
                hwExportTitle: "Exporting from Oven", hwExportDesc: "Connect a USB drive to the oven. Go to the 'Settings' - 'Import/Export from USB' and touch 'Export all recipes'. This will transfer all recipes to the USB stick to export/recipes/chef folder.",
                hwImportTitle: "Importing to Oven", hwImportDesc: "Connect a USB drive to the oven. Go to the 'Settings' - 'Import/Export from USB' and touch 'Import all recipes'. Recipes will be transfered to your oven.",
                disconnected: "Database not selected", connected: "Connected to recipe database", initBtn: "Select database location",
                addRecipe: "Add New Recipe", restoreBackup: "Restore from Backup", editorTitle: "Recipe Editor",
                recipeName: "Recipe Name", recipeImage: "Recipe Image", changeImg: "Change Image",
                imgNote: "Image will be cropped to 205x150px size.", selectCategory: "Select Category",
                preheat: "Pre-heating", hold: "Hold temperature", addStep: "Add phase", cancel: "Cancel", save: "Save",
                preheatDesc: "Automatic increases temperature for 40°C. When preheating temperature is reached you will hear buzzer. Once you open and close the oven doors, cooking will start. Max temperature in the oven is 270°C.",
                holdDesc: "Holds temperature at 80°C in the last step to keep food warm until served.",
                pulseTitle: "Pulse (Semi-static) Mode", pulseDesc: "Allows motors to be activated only when heating elements are operating. Reproduces static oven operation.",
                probeEx: "Note: You can only define one temperature parameter for core probe at a time.", probe: "Core probe temperature (°C)", delta: "Delta T for Core probe (°C)",
                hours: "Hours", minutes: "Minutes", temp: "Temperature", hum: "Humidity", fan: "Fan Speed",
                deleteConfirm: "Delete recipe?", minTime: "Each phase must last at least 1 minute!",
                phaseTitle: "Phases (Max 4)", askBackup: "Create a backup?",
                backupSuccess: "Backup created!", restorePrompt: "Select backup file:", advancedBtn: "Advanced cooking options"
            },
            it: {
                appWelcome: "Benvenuti in Recipe editor pro",
                appIntro: "Semplice applicazione web per la gestione delle ricette sui forni Tecnoeka touchscreen (TS). Aggiungi, modifica e rimuovi le ricette con facilità.",
                step1Title: "Seleziona database", step1Desc: "Seleziona la posizione della cartella <b>'chef'</b> dalle tue ricette esportate.",
                step2Title: "Consenti l'accesso", step2Desc: "Accetta la richiesta del browser per accedere e sincronizzare le modifiche direttamente nel database delle ricette.",
                step3Title: "Modifica e Salva", step3Desc: "Tutte le modifiche alle ricette vengono salvate direttamente nel database.",
                hardwareGuideTitle: "Come esportare e importare ricette dai forni Tecnoeka",
                hwExportTitle: "Esportazione dal forno", hwExportDesc: "Collega una chiavetta USB al forno. Vai su 'Impostazioni' - 'Importa/Esporta da USB' e tocca 'Esporta tutte le ricette'. Questo trasferirà tutte le ricette sulla chiavetta USB nella cartella export/recipes/chef.",
                hwImportTitle: "Importazione nel forno", hwImportDesc: "Collega una chiavetta USB al forno. Vai su 'Impostazioni' - 'Importa/Esporta da USB' e tocca 'Importa tutte le ricette'. Le ricette verranno trasferite nel forno.",
                disconnected: "Database non selezionato", connected: "Connesso al database delle ricette", initBtn: "Seleziona posizione database",
                addRecipe: "Aggiungi nuova ricetta", restoreBackup: "Ripristina da backup", editorTitle: "Editor Ricette",
                recipeName: "Nome Ricetta", recipeImage: "Immagine Ricetta", changeImg: "Cambia Immagine",
                imgNote: "L'immagine verrà ritagliata alla dimensione 205x150px.", selectCategory: "Seleziona Categoria",
                preheat: "Preriscaldamento", hold: "Mantenimento temperatura", addStep: "Aggiungi Fase", cancel: "Annulla", save: "Salva",
                preheatDesc: "Aumenta automaticamente la temperatura di 40°C. Al raggiungimento della temperatura di preriscaldamento si attiverà il segnale acustico. Una volta aperte e chiuse le porte del forno, inizierà la cottura. La temperatura massima nel forno è di 270°C.",
                holdDesc: "Mantiene la temperatura a 80°C nell'ultima fase per tenere il cibo caldo fino al servizio.",
                pulseTitle: "Modalità Pulse (Semi-statica)", pulseDesc: "Consente l'attivazione dei motori solo quando gli elementi riscaldanti sono in funzione. Riproduce il funzionamento di un forno statico.",
                probeEx: "Nota: È possibile definire solo un parametro di temperatura per la sonda al cuore alla volta.", probe: "Temperatura sonda al cuore (°C)", delta: "Delta T per sonda al cuore (°C)",
                hours: "Ore", minutes: "Minuti", temp: "Temperatura", hum: "Umidità", fan: "Velocità ventola",
                deleteConfirm: "Eliminare la ricetta?", minTime: "Ogni fase deve durare almeno 1 minuto!",
                phaseTitle: "Fasi (Max 4)", askBackup: "Creare un backup?",
                backupSuccess: "Backup creato!", restorePrompt: "Seleziona file di backup:", advancedBtn: "Opzioni di cottura avanzate"
            }
        };

        let db = null, dirHandle = null, dbFileHandle = null, currentLang = 'en';
        let categories = {}, currentImageBlob = null, phaseCount = 0;
        const catIcons = { 0:"fa-plate-wheat", 1:"fa-seedling", 2:"fa-cow", 3:"fa-drumstick-bite", 4:"fa-paw", 5:"fa-fish", 6:"fa-carrot", 7:"fa-cake-candles", 8:"fa-bread-slice" };

        async function init() { 
            window.SQL = await initSqlJs({ locateFile: f => `https://cdnjs.cloudflare.com/ajax/libs/sql.js/1.8.0/${f}` });
            changeLanguage('en'); 
        }
        init();

        function changeLanguage(lang) {
            currentLang = lang;
            document.querySelectorAll('[data-i18n]').forEach(el => {
                const key = el.getAttribute('data-i18n');
                if (i18nData[lang][key]) el.innerHTML = i18nData[lang][key];
            });
            if (db) { loadCategories(); renderRecipes(); }
        }

        async function initProject() {
            try {
                dirHandle = await window.showDirectoryPicker({ mode: 'readwrite' });
                dbFileHandle = await dirHandle.getFileHandle('chef.db');
                const file = await dbFileHandle.getFile();
                db = new SQL.Database(new Uint8Array(await file.arrayBuffer()));
                document.getElementById('dbStatus').innerHTML = `<span class="w-2 h-2 rounded-full bg-emerald-500"></span> ${i18nData[currentLang].connected}`;
                document.getElementById('initBtn').classList.add('hidden');
                document.getElementById('actionBtns').classList.remove('hidden');
                document.getElementById('welcomeScreen').classList.add('hidden');
                loadCategories(); renderRecipes();
                setTimeout(() => { if(confirm(i18nData[currentLang].askBackup)) createBackup(); }, 500);
            } catch (err) { alert("Init failed."); }
        }

        async function createBackup() {
            try {
                const handle = await window.showSaveFilePicker({ suggestedName: 'chef_backup.db.bak' });
                const writable = await handle.createWritable();
                await writable.write(db.export()); await writable.close();
                alert(i18nData[currentLang].backupSuccess);
            } catch(e) {}
        }

        async function restoreFromBackup() {
            try {
                const [handle] = await window.showOpenFilePicker();
                const writable = await dbFileHandle.createWritable();
                await writable.write(await (await handle.getFile()).arrayBuffer());
                await writable.close(); location.reload();
            } catch(e) {}
        }

        function loadCategories() {
            const col = currentLang === 'hr' ? 'cat_name_lang12' : (currentLang === 'it' ? 'cat_name_lang1' : 'cat_name_lang21');
            const res = db.exec(`SELECT id, ${col} FROM category_t`);
            const picker = document.getElementById('categoryPicker'); picker.innerHTML = '';
            if (res.length) {
                res[0].values.forEach(row => {
                    categories[row[0]] = row[1];
                    const btn = document.createElement('div');
                    btn.className = `cat-card p-2 rounded-2xl shadow-sm border border-slate-100 text-center`;
                    btn.id = `cat_item_${row[0]}`; btn.onclick = () => selectCategory(row[0]);
                    btn.innerHTML = `<i class="fas ${catIcons[row[0]] || "fa-utensils"} text-lg mb-1"></i><span class="text-[7px] font-black uppercase leading-tight block w-full px-1">${row[1]}</span>`;
                    picker.appendChild(btn);
                });
            }
            selectCategory(0);
        }

        function selectCategory(id) {
            document.querySelectorAll('.cat-card').forEach(el => el.classList.remove('selected'));
            const selected = document.getElementById(`cat_item_${id}`);
            if (selected) selected.classList.add('selected');
            document.getElementById('selected_cat_id').value = id;
        }

        function renderRecipes() {
            const grid = document.getElementById('recipeGrid'); grid.innerHTML = '';
            const res = db.exec("SELECT id, name_lang_1, cat_id, phases_cnt FROM recipes_t");
            if (!res.length) return;
            res[0].values.forEach(row => {
                const card = document.createElement('div');
                card.className = "bg-white p-6 rounded-[32px] border border-slate-200 shadow-sm hover:border-blue-600 cursor-pointer transition-all group relative";
                card.onclick = () => editRecipe(row[0]);
                card.innerHTML = `
                    <div class="flex justify-between items-start mb-6">
                        <div class="w-12 h-12 bg-slate-50 rounded-2xl flex items-center justify-center text-slate-400 group-hover:text-blue-600 transition-all"><i class="fas ${catIcons[row[2]] || "fa-utensils"} text-xl"></i></div>
                        <button onclick="event.stopPropagation(); deleteRecipe(${row[0]})" class="w-10 h-10 rounded-xl hover:bg-red-50 hover:text-red-500 flex items-center justify-center transition-all"><i class="fas fa-trash-alt text-sm"></i></button>
                    </div>
                    <h3 class="text-md font-bold text-slate-800 truncate pr-2">${row[1]}</h3>
                    <div class="flex justify-between items-center mt-6">
                        <span class="text-[9px] font-black text-blue-600 uppercase tracking-widest">${categories[row[2]] || 'General'}</span>
                        <span class="text-[10px] font-bold text-slate-300 uppercase">${row[3]} Steps</span>
                    </div>
                `;
                grid.appendChild(card);
            });
        }

        async function processImage(input) {
            const file = input.files[0]; if (!file) return;
            const img = new Image(); img.src = URL.createObjectURL(file);
            img.onload = () => {
                const canvas = document.createElement('canvas'); canvas.width = 205; canvas.height = 150;
                const ctx = canvas.getContext('2d');
                const ratio = Math.max(205/img.width, 150/img.height);
                const w = img.width*ratio, h = img.height*ratio;
                ctx.drawImage(img, (205-w)/2, (150-h)/2, w, h);
                canvas.toBlob(b => { currentImageBlob = b; document.getElementById('imgPreview').src = URL.createObjectURL(b); }, 'image/png');
            };
        }

        function handleProbeLogic(el, otherName) {
            const card = el.closest('.step-card');
            const other = card.querySelector(`[name="${otherName}"]`);
            const warning = card.querySelector('.probe-warning');
            const val = parseFloat(el.value) || 0;
            if (val > 0) { other.value = 0; other.disabled = true; warning.classList.remove('hidden'); }
            else { other.disabled = false; warning.classList.add('hidden'); }
        }

        function updateStepNumbers() {
            const list = document.getElementById('phasesList');
            Array.from(list.children).forEach((child, idx) => {
                child.querySelector('.step-num').innerText = `Step ${idx + 1}`;
            });
            document.getElementById('addPhaseBtn').style.display = phaseCount >= 4 ? 'none' : 'block';
        }

        function addPhase(data = null) {
            if (phaseCount >= 4) return;
            const container = document.getElementById('phasesList');
            const pId = "phase_" + Math.random().toString(36).slice(2);
            const div = document.createElement('div');
            div.className = "step-card p-8 relative shadow-sm"; div.id = pId;
            const h=data?data[3]:0, m=data?data[4]:15, t=data?data[5]:160, hu=data&&data[8]==110?0:(data?data[8]:0);
            const mot=data?data[9]:3, hr=data?data[6]:0, dt=data?data[7]:0, pl=data?data[10]:0;

            div.innerHTML = `
                <div class="flex justify-between items-center mb-8">
                    <span class="bg-slate-800 text-white px-5 py-1.5 rounded-full text-[9px] font-black uppercase tracking-widest step-num">Step</span>
                    <button type="button" onclick="removePhase('${pId}')" class="text-slate-200 hover:text-red-500 transition"><i class="fas fa-circle-xmark text-2xl"></i></button>
                </div>
                <div class="grid grid-cols-1 lg:grid-cols-3 gap-10">
                    <div class="bg-slate-100/50 p-8 rounded-[32px] flex items-center justify-center border border-white">
                        <div class="flex items-center gap-4">
                            <div class="text-center"><input type="number" name="hh" min="0" max="11" value="${h}" class="bg-transparent text-4xl font-black w-16 text-center outline-none"><p class="text-[8px] font-bold text-slate-400 uppercase" data-i18n="hours">Hours</p></div>
                            <span class="text-2xl font-black text-slate-200 mb-6">:</span>
                            <div class="text-center"><input type="number" name="mm" min="1" max="59" value="${m}" class="bg-transparent text-4xl font-black w-16 text-center outline-none"><p class="text-[8px] font-bold text-slate-400 uppercase" data-i18n="minutes">Minutes</p></div>
                        </div>
                    </div>
                    <div class="lg:col-span-2 space-y-8 py-2">
                        <div class="space-y-3">
                            <div class="flex justify-between items-end"><span class="text-[9px] font-black uppercase text-slate-400 tracking-widest" data-i18n="temp">Temperature</span><span class="text-2xl font-black text-slate-800"><span id="v_temp_${pId}">${t}</span>°C</span></div>
                            <input type="range" name="temp" min="30" max="270" value="${t}" class="w-full" oninput="document.getElementById('v_temp_${pId}').innerText = this.value">
                        </div>
                        <div class="space-y-3">
                            <div class="flex justify-between items-end"><span class="text-[9px] font-black uppercase text-slate-400 tracking-widest" data-i18n="hum">Humidity</span><span class="text-2xl font-black text-slate-800"><span id="v_hum_${pId}">${hu}</span>%</span></div>
                            <input type="range" name="hum" min="0" max="100" step="10" value="${hu}" class="w-full" oninput="document.getElementById('v_hum_${pId}').innerText = this.value">
                        </div>
                        <div class="space-y-3">
                            <div class="flex justify-between items-end"><span class="text-[9px] font-black uppercase text-slate-400 tracking-widest" data-i18n="fan">Fan Speed</span><span class="text-2xl font-black text-slate-800"><span id="v_fan_${pId}">${mot}</span></span></div>
                            <input type="range" name="motor" min="1" max="5" value="${mot}" class="w-full" oninput="document.getElementById('v_fan_${pId}').innerText = this.value">
                        </div>
                    </div>
                </div>
                <div class="mt-8 pt-6 border-t border-slate-50">
                    <button type="button" onclick="this.nextElementSibling.classList.toggle('open')" class="text-[9px] font-black text-slate-400 uppercase flex items-center gap-2 hover:text-blue-600 transition tracking-widest" data-i18n="advancedBtn"></button>
                    <div class="accordion-content">
                        <div class="space-y-6">
                            <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
                                <div class="bg-slate-50 p-4 rounded-2xl relative border border-slate-100"><label class="text-[8px] font-bold text-slate-400 uppercase tracking-widest" data-i18n="probe"></label><input type="number" name="heart" min="0" max="100" value="${hr}" oninput="handleProbeLogic(this, 'deltaT')" class="w-full bg-transparent font-bold mt-1 outline-none"></div>
                                <div class="bg-slate-50 p-4 rounded-2xl relative border border-slate-100"><label class="text-[8px] font-bold text-slate-400 uppercase tracking-widest" data-i18n="delta"></label><input type="number" name="deltaT" min="0" max="100" value="${dt}" oninput="handleProbeLogic(this, 'heart')" class="w-full bg-transparent font-bold mt-1 outline-none"></div>
                            </div>
                            <p class="probe-warning text-[8px] text-orange-500 font-bold uppercase hidden" data-i18n="probeEx"></p>
                            <div class="bg-white p-6 rounded-[28px] border-2 border-slate-100 shadow-sm">
                                <label class="flex items-center justify-between cursor-pointer group mb-2"><span class="text-[10px] font-black uppercase text-slate-500 group-hover:text-blue-600 transition" data-i18n="pulseTitle"></span><div class="relative"><input type="checkbox" name="pulse" class="sr-only peer" ${pl==1?'checked':''}><div class="w-11 h-6 bg-slate-200 rounded-full peer peer-checked:bg-blue-600 peer-checked:after:translate-x-full after:content-[''] after:absolute after:top-[2px] after:left-[2px] after:bg-white after:rounded-full after:h-5 after:w-5 after:transition-all shadow-inner border border-slate-300"></div></div></label>
                                <p class="info-text" data-i18n="pulseDesc"></p>
                            </div>
                        </div>
                    </div>
                </div>
            `;
            container.appendChild(div); phaseCount++; updateStepNumbers(); changeLanguage(currentLang);
            if(hr>0) handleProbeLogic(div.querySelector('[name=heart]'), 'deltaT');
            if(dt>0) handleProbeLogic(div.querySelector('[name=deltaT]'), 'heart');
        }

        function removePhase(id) { document.getElementById(id).remove(); phaseCount--; updateStepNumbers(); }
        
        async function openModal() {
            document.getElementById('recipeForm').reset();
            document.getElementById('recipeId').value='';
            document.getElementById('existing_img_name').value='ricetta.png';
            document.getElementById('phasesList').innerHTML='';
            currentImageBlob=null; phaseCount=0; selectCategory(0);
            try {
                const imgsFolder = await dirHandle.getDirectoryHandle('imgs');
                const file = await (await imgsFolder.getFileHandle('ricetta.png')).getFile();
                document.getElementById('imgPreview').src = URL.createObjectURL(file);
            } catch(e) { document.getElementById('imgPreview').src = ''; }
            addPhase();
            document.getElementById('modal').classList.remove('hidden');
        }

        function closeModal() { document.getElementById('modal').classList.add('hidden'); }

        async function editRecipe(id) {
            await openModal();
            const r = db.exec(`SELECT * FROM recipes_t WHERE id = ${id}`)[0].values[0];
            document.getElementById('recipeId').value = r[1];
            document.getElementById('name_lang_1').value = r[2];
            document.getElementById('preheat').checked = r[63] == 1;
            document.getElementById('hold').checked = r[64] == 1;
            document.getElementById('existing_img_name').value = r[67] || 'ricetta.png';
            selectCategory(r[0]);
            try {
                const imgsFolder = await dirHandle.getDirectoryHandle('imgs');
                const file = await (await imgsFolder.getFileHandle(r[67] || 'ricetta.png')).getFile();
                document.getElementById('imgPreview').src = URL.createObjectURL(file);
            } catch(e) {}
            document.getElementById('phasesList').innerHTML = ''; phaseCount = 0;
            const pRes = db.exec(`SELECT * FROM phases_t WHERE recip_id = ${id} ORDER BY id ASC`);
            if (pRes.length && pRes[0].values) pRes[0].values.forEach(p => addPhase(p));
        }

        document.getElementById('recipeForm').onsubmit = async function(e) {
            e.preventDefault();
            const name = document.getElementById('name_lang_1').value;
            const rId = document.getElementById('recipeId').value;
            let imgName = document.getElementById('existing_img_name').value;
            if (currentImageBlob) {
                imgName = `${name.toLowerCase().replace(/\s+/g, '_')}.png`;
                const imgsFolder = await dirHandle.getDirectoryHandle('imgs', { create: true });
                const writable = await (await imgsFolder.getFileHandle(imgName, { create: true })).createWritable();
                await writable.write(currentImageBlob); await writable.close();
            }
            const phases = []; let valid = true;
            document.querySelectorAll('#phasesList > div').forEach(el => {
                const h=parseInt(el.querySelector('[name="hh"]').value)||0, m=parseInt(el.querySelector('[name="mm"]').value)||0;
                if(h===0 && m < 1) valid=false; // VALIDACIJA: MIN 1 MINUTA
                const hum=parseInt(el.querySelector('[name="hum"]').value);
                phases.push({h,m,t:el.querySelector('[name="temp"]').value,hu:hum===0?110:hum,mot:el.querySelector('[name="motor"]').value,hr:el.querySelector('[name="heart"]').value,dt:el.querySelector('[name="deltaT"]').value,pl:el.querySelector('[name="pulse"]').checked?1:0});
            });
            if(!valid){ alert(i18nData[currentLang].minTime); return; }
            try {
                if(rId){
                    db.run(`UPDATE recipes_t SET name_lang_1=?, cat_id=?, phases_cnt=?, src_image=?, preheat=?, hold=? WHERE id=?`, [name, document.getElementById('selected_cat_id').value, phases.length, imgName, document.getElementById('preheat').checked?1:0, document.getElementById('hold').checked?1:0, rId]);
                    db.run(`DELETE FROM phases_t WHERE recip_id=?`, [rId]);
                } else {
                    db.run(`INSERT INTO recipes_t (cat_id, name_lang_1, phases_cnt, src_image, type, preheat, hold, usage) VALUES (?,?,?,?,0,0,0,0)`, [document.getElementById('selected_cat_id').value, name, phases.length, imgName, document.getElementById('preheat').checked?1:0, document.getElementById('hold').checked?1:0]);
                }
                const newId = rId || db.exec("SELECT last_insert_rowid()")[0].values[0][0];
                phases.forEach((p, idx) => db.run(`INSERT INTO phases_t (recip_id, id, cook_mode, hh, mm, temp, heart, deltaT, hum, motor, pulse) VALUES (?,?,0,?,?,?,?,?,?,?,?)`, [newId, idx, p.h, p.m, p.t, p.hr, p.dt, p.hu, p.mot, p.pl]));
                const writable = await dbFileHandle.createWritable();
                await writable.write(db.export()); await writable.close();
                renderRecipes(); closeModal();
            } catch(err) { alert(i18nData[currentLang].saveError + err.message); }
        };

        async function deleteRecipe(id) {
            if (confirm(i18nData[currentLang].deleteConfirm)) {
                db.run("DELETE FROM recipes_t WHERE id=?", [id]);
                db.run("DELETE FROM phases_t WHERE recip_id=?", [id]);
                const writable = await dbFileHandle.createWritable();
                await writable.write(db.export()); await writable.close();
                renderRecipes();
            }
        }
    </script>
</body>
</html>

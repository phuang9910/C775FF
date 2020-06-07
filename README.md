
<html lang="en">
<head>
    <title>Accuband C775FF Calculation</title>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <!-- Latest compiled and minified CSS -->
    <link rel="stylesheet"
          href="https://maxcdn.bootstrapcdn.com/bootstrap/4.4.1/css/bootstrap.min.css">
    <!-- jQuery library -->
    <script src="https://ajax.googleapis.com/ajax/libs/jquery/3.4.1/jquery.min.js"></script>
    <!-- Popper JS -->
    <script src="https://cdnjs.cloudflare.com/ajax/libs/popper.js/1.16.0/umd/popper.min.js"></script>
    <!-- Latest compiled JavaScript -->
    <script src="https://maxcdn.bootstrapcdn.com/bootstrap/4.4.1/js/bootstrap.min.js"></script>
</head>


<body>

    <div class="row">
        <div class="col-2 text-center">
        </div>
        <!-- Input Minimum Strip Width -->
        <!-- Input Maximum Strip Width -->
        <div class="col-4 text-center">
            <br>
            <!-- Input Minimum Strip Width -->
            <div class="input-group mb-3">
                <div class="input-group-prepend">
                    <span class="input-group-text"> Minimum Strip Width:</span>
                </div>
                <input type="text" class="form-control" id="minWidth" value="600">
                <span class="input-group-text"> mm </span>
            </div>
            <!-- Input Maximum Strip Width -->
            <div class="input-group mb-3">
                <div class="input-group-prepend">
                    <span class="input-group-text"> Maximum Strip Width:</span>
                </div>
                <input type="text" class="form-control" id="maxWidth" value="1800">
                <span class="input-group-text"> mm </span>
            </div>
        </div>
        <!-- Input Maximum  CLD -->
        <!-- Input Maximum HOP -->
        <!-- Input Preferred Installation Height -->

        <div class="col-4 text-center">
            <br />
            <div class="input-group mb-3 input-group-sm">
                <div class="input-group-prepend">
                    <span class="input-group-text">Maximum  CLD:</span>
                </div>
                <input type="text" class="form-control" id="maxCLD" value="">
                <div class="input-group-append">
                    <span class="input-group-text"> mm </span>
                </div>
            </div>

            <div class="input-group mb-3 input-group-sm">
                <div class="input-group-prepend">
                    <span class="input-group-text" id="basic-addon1">Maximum HOP:</span>
                </div>
                <input type="text" class="form-control" id="maxHOP">
                <div class="input-group-append">
                    <span class="input-group-text"> mm </span>
                </div>
            </div>

            <div class="input-group mb-3 input-group-sm">
                <div class="input-group-prepend">
                    <span class="input-group-text" id="basic-addon1">Preferred Installation Height:</span>
                </div>
                <input type="text" class="form-control" id="PreferredHeight">
                <div class="input-group-append">
                    <span class="input-group-text"> mm </span>
                </div>
            </div>
        </div>

        <div class="col-2 text-center">
        </div>

    </div>

    <!-- Button calculate -->
    <div class="row">
        <div class="col-6 text-center">
            <button type="button" id="calculate" onclick="calculate();">Calculate</button> <br> <BR> <BR>
        </div>
    </div>


    <div class="row">
        <div class="col-2 text-center">
        </div>
        <div class="col-4 text-center">
            <div class="input-group mb-3 input-group-sm">
                <div class="input-group-prepend">
                    <label class="input-group-text" for="inputGroupSelect01">Scanner Orientation:</label>
                </div>
                <select class="selOrientation" id="selOrientation">
                    <option value="" disabled selected>Choose</option>
                    <option value="LEFT">Left</option>
                    <option value="RIGHT">Right</option>
                </select>
            </div>
            <div class="input-group mb-3 input-group-sm">
                <div class="input-group-prepend">
                    <label class="input-group-text" for="inputGroupSelect02">Communication Protocol:</label>
                </div>
                <select class="HostCommunicationProtocol" id="HostCommunicationProtocol">
                    <option value="TS-542">TS-542</option>
                    <option value="TBD">TBD</option>
                </select>

            </div>

            <br>

        </div>



        <div class="col-4 text-center">

            <div class="input-group mb-3 input-group-sm">
                <div class="input-group-prepend">
                    <span class="input-group-text">Lens Focus Length:</span>
                </div>
                <input type="text" class="form-control" id="lensFocus" placeholder="LENS" aria-label="lensFocusLength" aria-describedby="basic-addon1" disabled>
                <div class="input-group-append">
                    <span class="input-group-text">mm</span>
                </div>
            </div>
            <div class="input-group mb-3 input-group-sm">
                <div class="input-group-prepend">
                    <span class="input-group-text">Installation Height:</span>
                </div>
                <input type="text" class="form-control" id="instHeight" placeholder="HEIGHT" aria-label="InstallationHeight" aria-describedby="basic-addon1" disabled>
                <div class="input-group-append">
                    <span class="input-group-text">mm</span>
                </div>
            </div>
            <div class="input-group mb-3 input-group-sm">
                <div class="input-group-prepend">
                    <span class="input-group-text">Camera Separation:</span>
                </div>
                <input type="text" class="form-control" id="cameraSeparation" placeholder="SEP" aria-label="CameraSeparation" aria-describedby="basic-addon1" disabled>
                <div class="input-group-append">
                    <span class="input-group-text">mm</span>
                </div>
            </div>
        </div>
        <div class="col-2 text-center">
        </div>
    </div>


    <div class="row">
        <div class="col-1 text-center">
        </div>
        <div class="col-5 text-center">
            <div class="input-group mb-3 input-group-sm">

                <div class="input-group-prepend">
                    <label class="input-group-text" for="inputGroupSelect03">ProfiBUS/ProfiNet Option</label>
                </div>
                <select class="ProfiOption" id="ProfiOption">
                    <option value="">Not Used</option>
                    <option value="PL059823-DCPB">PROFIBUS, Installed in PS&P Unit</option>
                    <option value="PL059823-DCPBM">PROFIBUS, 1M/C Installed in PS&P Unit</option>
                    <option value="PL059823-DCPBMM">PROFIBUS, 2M/C Installed in PS&P Unit</option>
                    <option value="PL059823-ACPB">PROFIBUS, Field Installation</option>
                    <option value="PL059823-ACPBM">PROFIBUS, 1M/C Field Installation</option>
                    <option value="PL059823-ACPBMM">PROFIBUS, 2M/C Field Installation</option>
                    <option value="PL059823-DCPN">PROFINET, Installed in PS&P Unit</option>
                    <option value="PL059823-DCPNM">PROFINET, 1M/C Installed in PS&P Unit</option>
                    <option value="PL059823-DCPNMM">PROFINET, 2M/C Installed in PS&P Unit</option>
                    <option value="PL059823-ACPN">PROFINET, Field Installation</option>
                    <option value="PL059823-ACPNM">PROFINET, 1M/C Field Installation</option>
                    <option value="PL059823-ACPNMM">PROFINET, 2M/C Field Installation</option>
                </select>
                <br />
            </div>
            <div class="input-group mb-3 input-group-sm">
                <div class="input-group-prepend">
                    <label class="input-group-text" for="inputGroupSelect04">Discrete IO Option</label>
                </div>
                <select class="DiscreteIO" id="DiscreteIO" name="DiscreteIO">
                    <option value="">Not Used </option>
                    <option value="PL059820-VVW-18">IN:+/-10V; OUT: +/-10V</option>
                    <option value="PL059820-VCW-18">IN:+/-10V; OUT: 4-20mA</option>
                    <option value="PL059820-CVW-18">IN:4-20mA; OUT: +/-10V</option>
                    <option value="PL059820-CCW-18">IN:4-20mA; OUT: 4-20mA</option>
                    <option value="PL059820-VVWM-18">IN:+/-10V; OUT: +/-10V 1M/C</option>
                    <option value="PL059820-VCWM-18">IN:+/-10V; OUT: 4-20mA 1M/C</option>
                    <option value="PL059820-CVWM-18">IN:4-20mA; OUT: +/-10V 1M/C</option>
                    <option value="PL059820-CCWM-18">IN:4-20mA; OUT: 4-20mA 1M/C</option>
                </select>

            </div>

        </div>
        <div class="col-4 text-center">

            <span class="input-group-text">Calculated Field of View</span>

            <div class="input-group-prepend">
                <span class="input-group-text">@ max HOP:</span>

                <input type="text" class="form-control" id="minFOVatHOP" placeholder="MIN" aria-label="minFOVatHOP" aria-describedby="basic-addon1">
                <span class="input-group-text">mm</span>

                <input type="text" class="form-control" id="maxFOVatHOP" placeholder="MAX" aria-label="maxFOVatHOP" aria-describedby="basic-addon1">
                <span class="input-group-text">mm</span>

            </div>

            <div class="input-group-prepend">
                <span class="input-group-text">@ Pass Line:</span>

                <input type="text" class="form-control" id="minFOVPassline" placeholder="MIN" aria-label="minFOVPassline" aria-describedby="basic-addon1">
                <span class="input-group-text">mm</span>

                <input type="text" class="form-control" id="maxFOVPassline" placeholder="MAX" aria-label="maxFOVPassline" aria-describedby="basic-addon1">
                <span class="input-group-text">mm</span>

            </div>

        </div>
        <div class="col-2 text-center">
        </div>
    </div>

    <div class="row">
        <div class="col-6 text-center">
            <button type="button" id="downloadcsv" onclick="download_csv();">Create WorkOrder </button>
        </div>
    </div>

</body>
</html>


<script>

    var Camber = 3.0  // fixed camera camber angle
    var CCD = 28.672 * (2048 - 24) / 2048  //edges are not detected in the first and last 12 pixels of CCD.
    var viewingAngle
    var angleAA


    var minHeight = 900
    var maxHeight = 1600
    
    var defaultCLD = 50
    var defaultHOP = 30

    var LensFocusLength
    var RequiredCameraSeparation
    var InstallationHeight


 //   var PreferredHeight
    var LineItem = [
        ['1', ' ', ' ', ' ', ' ', ' ', ' ', ' ', ' ', ' ', ' ', ' ', ' ']
    ];
    var C775ItemA = [
        ['1', 'A', '1', 'EA', 'C775FF-2500-50-L-A', 'ACCUBAND C775FF Width GAGE', ' ', 'MFG', ' ', ' ', ' ', ' ', ' '],
        ['2', 'A1', '1', 'EA', 'PL059338-2500-', 'Accuband C775FF SCANNER ASSEMBLY 2500mm ', ' ', 'PRD', ' ', ' ', ' ', ' ', '1'],
        ['3', 'A2', '2', 'EA', 'PL059180-50 ', 'STEREO CAMERA ASSEMBLY 50mm FL ', ' ', 'PRD', ' ', ' ', ' ', ' ', '1'],
        ['4', 'A3', '2', 'EA', 'PL059655', 'Nozzle AssemblyAccuband C775FF NOZZLE ASSEMBLY', ' ', 'PRD', ' ', ' ', ' ', ' ', '1'],
        ['5', 'A4', '2', 'EA', 'PL059495', 'Accuband C775FF FRONT LIGHT ASSEMBLY 1200mm', ' ', 'PRD', ' ', ' ', ' ', ' ', '1'],
        ['6', 'A5', '2', 'EA', 'PL059344', 'ACCUBAND C775FF COVER', ' ', 'PRD', ' ', ' ', ' ', ' ', '1'],
        ['7', 'A6', '1', 'EA', 'PL059527', 'Accuband C775FF POWER SUPPLY & PROCESSOR ASSEMBLY', ' ', 'PRD', ' ', ' ', ' ', ' ', '2'],
        ['8', 'A7', '1', 'EA', 'PL057296', 'Accuband C775FF CALIBRATOR SUPPORT KIT', ' ', 'PRD', ' ', ' ', ' ', ' ', '1'],
        ['9', 'A8', '1', 'EA', 'PL059771', 'Accuband C775FF Accessary kit', ' ', 'PRD', ' ', ' ', ' ', ' ', '1'],
        ['10', 'A9', '1', 'EA', '059772-1', 'Installation Information Label :CAMERA SEPARATION: 1475 mm INSTALLATION HEIGHT: 1190 mm ', ' ', 'REF', ' ', ' ', ' ', ' ', ''],
        ['11', ' ', ' ', ' ', ' ', ' ', ' ', ' ', ' ', ' ', ' ', ' ', ' ']
    ];
    var C775ItemB = [
        ['1', 'B', '', 'EA', '', 'ACCUBAND CABINET OPTION', ' ', '', ' ', ' ', ' ', ' ', '']
    ];

    var C775ItemC = [
        ['1', 'C', '1', 'EA', 'C775FF-CAL-A', 'ACCUBAND C775FF CALIBRATION EQUIPMENT', ' ', 'MFG', ' ', ' ', ' ', ' ', '1'],
        ['2', 'C1', '1', 'EA', 'PL059235', 'Accuband C775FF LONG CALIBRATOR', ' ', 'PRD', ' ', ' ', ' ', ' ', ''],
        ['3', 'C2', '1', 'EA', 'PL059242 ', 'Accuband C775FF SHORT CALIBRATOR', ' ', 'PRD', ' ', ' ', ' ', ' ', ''],
        ['4', 'C3', '1', 'EA', '*09185', 'Accuband C775FF CALIBRATOR STORAGE CASE', ' ', 'PRD', ' ', ' ', ' ', ' ', ''],
        ['5', ' ', ' ', ' ', ' ', ' ', ' ', ' ', ' ', ' ', ' ', ' ', ' ']
    ];
    var C775ItemD = [
        ['1', 'D', '', 'EA', '', 'OPERATOR\'S INTERFACE', ' ', '', ' ', ' ', ' ', ' ', ''],
        ['2', ' ', ' ', ' ', ' ', ' ', ' ', ' ', ' ', ' ', ' ', ' ', ' ']
    ];
    var C775ItemG = [
        ['1', 'G', '', 'EA', '', 'ADDITIONAL FEATURE', ' ', '', ' ', ' ', ' ', ' ', ''],
        ['2', ' ', ' ', ' ', ' ', ' ', ' ', ' ', ' ', ' ', ' ', ' ', ' ']
    ];
    var C775ItemH = [
        ['1', 'H', '', 'EA', '', 'ENGINEERING SERVICE', ' ', '', ' ', ' ', ' ', ' ', ''],
        ['2', 'H1', '1', 'EA', '', 'Project Engineering', ' ', '', ' ', ' ', ' ', ' ', ''],
        ['3', ' ', ' ', ' ', ' ', ' ', ' ', ' ', ' ', ' ', ' ', ' ', ' ']
    ];
    var C775ItemJ = [
        ['1', 'J', '', 'EA', '', 'COMMISSIONING AND TRAINING', ' ', '', ' ', ' ', ' ', ' ', ''],
        ['2', ' ', ' ', ' ', ' ', ' ', ' ', ' ', ' ', ' ', ' ', ' ', ' ']
    ];
    var C775ItemK = [
        ['1', 'K', '', 'EA', '', 'DOCUMENTAION', ' ', '', ' ', ' ', ' ', ' ', ''],
        ['2', 'K1', '1', 'EA', '90512', 'Accuband C775-FF Width Gage User\'s Manuals', ' ', '', ' ', ' ', ' ', ' ', ''],
        ['3', 'K2', '1', 'EA', '59811', ' System Drawing Package', ' ', '', ' ', ' ', ' ', ' ', ''],
        ['4', 'K3', '1', 'EA', '', ' Documentation on KELK Network', ' ', '', ' ', ' ', ' ', ' ', ''],
        ['5', ' ', ' ', ' ', ' ', ' ', ' ', ' ', ' ', ' ', ' ', ' ', ' ']
    ];
    var C775ItemS = [
        ['1', 'S', '', 'EA', '', 'SOFTWARE', ' ', '', ' ', ' ', ' ', ' ', ''],
        ['2', 'S1', '1', 'EA', 'TS-542', 'Accuband V6 C775-FF Communication Protocol', ' ', 'ENG', ' ', ' ', ' ', ' ', ''],
        ['3', ' ', ' ', ' ', ' ', ' ', ' ', ' ', ' ', ' ', ' ', ' ', ' ']
    ];
    var C775ItemT = [
        ['1', 'G', '', 'EA', '', 'ADDITIONAL PRODUCTION TESTING', ' ', '', ' ', ' ', ' ', ' ', ''],
        ['2', ' ', ' ', ' ', ' ', ' ', ' ', ' ', ' ', ' ', ' ', ' ', ' ']
    ];

    document.getElementById("maxCLD").value = defaultCLD
    document.getElementById("maxHOP").value = defaultHOP



    function getViewingAngle(CCD,L) {
        //CCD: Effective CCD Length
        //L: Actual Focal Length
        var viewingAngle =2*Math.atan(CCD/(2*L))*180/Math.PI
        //2 * ATAN(CCD / (2 * L)) * 180 / PI()
        return viewingAngle
    }


    function getHeight(actualFocalLength, fov, spacing) {
        viewingAngle = 2 * Math.atan(CCD / (2 * actualFocalLength)) * 180 / Math.PI

        angleAA = viewingAngle / 2 - Camber // Camera A 1st Edge Angle
        var height = (fov - spacing) / (2 * Math.tan(angleAA * Math.PI / 180))
        return height
    }

    function getFOV(angle, height, spacing) {
        var fov = height * Math.tan(angle * Math.PI / 180) * 2 + spacing
        return fov
    }
    function calculate() {
        var installationHeightOffset = 79.5
        var maxPositionError = 20
        var cameraSeparation = 99.60  //camera A&B  or C&Dseparation

        var focalLength = [43.29, 52.85] //actual focal length for 40mm and 50mm LENS

        LensFocusLength = 50

        var PreferredHeight = parseInt(document.getElementById("PreferredHeight").value)

        if (PreferredHeight < minHeight) {

        }
        var minStripWidth = parseInt(document.getElementById("minWidth").value)

        var maxStripWidth = parseInt(document.getElementById("maxWidth").value)

        var maxCLD = parseInt(document.getElementById("maxCLD").value)
        var maxHOP = parseInt(document.getElementById("maxHOP").value)

        RequiredCameraSeparation = (minStripWidth + maxStripWidth)/2 // Camera AB & CD separation
        document.getElementById("cameraSeparation").value = RequiredCameraSeparation

        var cameraFOV = (maxStripWidth  - minStripWidth) / 2 + maxCLD + maxPositionError



        var cameraHeightaboveHOP = getHeight(focalLength[1], cameraFOV, cameraSeparation)

        InstallationHeight = cameraHeightaboveHOP + maxHOP + installationHeightOffset
//




        if ((InstallationHeight > maxHeight) || (InstallationHeight > PreferredHeight) && (PreferredHeight > minHeight)){
            LensFocusLength = 40
            cameraHeightaboveHOP = getHeight(focalLength[0], cameraFOV, cameraSeparation)
            InstallationHeight = cameraHeightaboveHOP + maxHOP + installationHeightOffset

        }



        if (InstallationHeight < minHeight) {
            InstallationHeight = minHeight
        }

        if (InstallationHeight < PreferredHeight) {
            InstallationHeight = PreferredHeight
        }


        InstallationHeight = Math.round(InstallationHeight)


        document.getElementById("lensFocus").placeholder = LensFocusLength
        document.getElementById("instHeight").placeholder = InstallationHeight
        document.getElementById("cameraSeparation").placeholder = RequiredCameraSeparation

        cameraHeightaboveHOP = InstallationHeight - maxHOP
        cameraFOV = Math.round(getFOV(angleAA, cameraHeightaboveHOP, cameraSeparation))-1
        maxStripWidth = RequiredCameraSeparation + cameraFOV
        minStripWidth = RequiredCameraSeparation - cameraFOV
        document.getElementById("minFOVatHOP").placeholder = minStripWidth
        document.getElementById("maxFOVatHOP").placeholder = maxStripWidth

        cameraFOV = Math.round(getFOV(angleAA, InstallationHeight, cameraSeparation))-1
        maxStripWidth = Math.round(RequiredCameraSeparation + cameraFOV)
        minStripWidth = Math.round(RequiredCameraSeparation - cameraFOV)
        document.getElementById("minFOVPassline").placeholder = minStripWidth
        document.getElementById("maxFOVPassline").placeholder = maxStripWidth

    }


    function prepare_lineItems() {
        var selectedOption

        // finalize orientation
        var selectedOrenitation = document.getElementById("selOrientation").value;
        C775ItemA[0][4] = "C775FF - 2500 - " + LensFocusLength + " - " + selectedOrenitation.substr(0, 1) + "- A";

        C775ItemA[1][4] = "PL059338 - 2500 - " + selectedOrenitation.substr(0, 1);
        C775ItemA[1][5] = "Accuband C775FF SCANNER ASSEMBLY 2500mm " + selectedOrenitation;
        C775ItemA[2][4] = "PL059180 - " + LensFocusLength;
        C775ItemA[2][5] = "STEREO CAMERA ASSEMBLY " + LensFocusLength + " FL";
        C775ItemA[9][5] = "Installation Information Label: CAMERA SEPARATION= " + RequiredCameraSeparation + "mm; " + "INSTALLATION HEIGHT=" + InstallationHeight + "mm";

        // Host Communication Option
        selectedOption = document.getElementById("HostCommunicationProtocol").value;
        C775ItemS[1][4] = selectedOption;
        switch (selectedOption) {
            case "TS-542":
                C775ItemS[1][5] = 'Accuband V6 C775 - FF Communication Protocol'
                break;
            case "TBD":
                C775ItemS[1][5] = 'TBD Communication Protocol'
                break;
                defaule:
                C775ItemS[1][5] = 'Communication Protocol';
        }

        C775ItemB = [
            ['1', 'B', '', 'EA', '', 'ACCUBAND CABINET OPTION', ' ', '', ' ', ' ', ' ', ' ', '']
        ];

        // discrete IO options
        selectedOption = document.getElementById("DiscreteIO").value;
        if (selectedOption != "") {
            LineItem[0] = C775ItemB.length+1
            LineItem[1] = "B" + C775ItemB.length
            LineItem[2] = '1'
            LineItem[3] = 'EA'
            LineItem[4] = document.getElementById("DiscreteIO").value;
            LineItem[5] = 'Accuband C775FF Discrete IO Assembly'
            LineItem[7] = 'PRD'
            LineItem[12] = '1'

            C775ItemB.push(LineItem.concat());
            console.log(C775ItemB)
        }

        // Profi Options 
        selectedOption = document.getElementById("ProfiOption").value;
        if (selectedOption != "") {
            LineItem[0] = C775ItemB.length+1
            LineItem[1] = "B" + C775ItemB.length
            LineItem[2] = '1'
            LineItem[3] = 'EA'
            LineItem[4] = document.getElementById("ProfiOption").value;
            LineItem[5] = 'Accuband C775FF ProfiBUS/ProfiNET Option'
            LineItem[7] = 'PRD'
            LineItem[12] = '1'
            C775ItemB.push(LineItem.concat());
            console.log(C775ItemB)
         }
        LineItem[0] = C775ItemB.length + 1
        LineItem[1] = ''
        LineItem[2] = ''
        LineItem[3] = ''
        LineItem[4] = ''
        LineItem[5] = ''
        LineItem[7] = ''
        LineItem[12] = ''
        C775ItemB.push(LineItem.concat());
        console.log(C775ItemB)


    }

    function download_csv() {
        var csv = 'C775FF,Item,QTY,UOM,PartNumber,Description,SN,Status,FolderDate,MFGDate,ShipDate,Tran,Crate\n';

        prepare_lineItems();


        C775Items = C775ItemA.concat(C775ItemB, C775ItemC, C775ItemD, C775ItemG, C775ItemH, C775ItemJ, C775ItemK, C775ItemS, C775ItemT);
            C775Items.forEach(function (row) {
                csv += row.join(',');
                csv += "\n";
            });

            console.log(csv);
            var hiddenElement = document.createElement('a');
            hiddenElement.href = 'data:text/csv;charset=utf-8,' + encodeURI(csv);
            hiddenElement.target = '_blank';
            hiddenElement.download = 'C775FF.csv';
            hiddenElement.click();
        }



    function execute(){

        document.getElementById("PreferredHeight").value = "have a nice day"


    }</script>




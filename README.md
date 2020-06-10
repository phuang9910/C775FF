<html lang="en">
<head>
    <title>Accuband C775FF Calculation</title>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <!-- Latest compiled and minified CSS -->
    <link rel="stylesheet"
          href="https://maxcdn.bootstrapcdn.com/bootstrap/4.4.1/css/bootstrap.min.css">
    <!-- jQuery library -->
    <script src="https://ajax.googleapis.com/ajax/libs/jquery/3.5.1/jquery.min.js"></script>
    <!-- Popper JS -->
    <script src="https://cdnjs.cloudflare.com/ajax/libs/popper.js/1.16.0/umd/popper.min.js"></script>
    <!-- Latest compiled JavaScript -->
    <script src="https://maxcdn.bootstrapcdn.com/bootstrap/4.4.1/js/bootstrap.min.js"></script>

    <style>
        .tooltip {
            position: relative;
            display: inline-block;
            border-bottom: 1px dotted black;
        }
        .tooltip-inner {
            white-space: pre-wrap;
        }
            .tooltip .tooltiptext {
                visibility: hidden;
                width: 120px;
                background-color: #555;
                color: #fff;
                text-align: center;
                border-radius: 6px;
                padding: 5px 0;
                position: absolute;
                z-index: 1;
                bottom: 125%;
                left: 50%;
                margin-left: -60px;
                opacity: 0;
                transition: opacity 0.3s;
            }

                .tooltip .tooltiptext::after {
                    content: "";
                    position: absolute;
                    top: 100%;
                    left: 50%;
                    margin-left: -5px;
                    border-width: 5px;
                    border-style: solid;
                    border-color: #555 transparent transparent transparent;
                }

            .tooltip:hover .tooltiptext {
                visibility: visible;
                opacity: 1;
            }


        .formDivA {
            padding: 10px;
            border: 5px;
            border-color: green;
            border-style: solid;
            border-top-style: solid;
            border-right-style: solid;
            border-bottom-style: solid;
            border-left-style: solid;
        }
        .formDivB {
            padding: 10px;
            border: 5px;
            border-color:cadetblue;
            border-style: solid;
            border-top-style: solid;
            border-right-style: solid;
            border-bottom-style: solid;
            border-left-style: solid;
        }
        .formDivC {
            padding: 10px;
            border: 5px;
            border-color: lightgrey;
            border-style: solid;
            border-top-style: solid;
            border-right-style: solid;
            border-bottom-style: solid;
            border-left-style: solid;
        }
        input:invalid {
            border: 2px dashed red;
        }

        input:invalid:required {
            border: 2px dashed green;
        }

        input:valid {
            border: 1px solid black;
        }
 
        /* Style the button that is used to open and close the collapsible content */
        .collapsible {
            background-color: #4CAF50;
            color: white;
            cursor: pointer;
            padding: 10px;
            width: 10%;
            border: none;
            text-align: center;
            outline: none;
            font-size: 15px;
        }

            /* Add a background color to the button if it is clicked on (add the .active class with JS), and when you move the mouse over it (hover) */
        .active, .collapsible:hover {
                background-color: lightgreen;
        }

        /* Style the collapsible content. Note: hidden by default */
        .content {
            padding: 0 18px;
            display: none;
            overflow: hidden;
            background-color: #f1f1f1;
        }

    </style>


</head>


<body>
    <div class="row">
        <div class="col-2 text-center">
        </div>
        <!-- Input Minimum Strip Width -->
        <!-- Input Maximum Strip Width -->
        <div class="col-4 text-center">
            <h3 style="color: green;">1. Input Data</h3>


            <div class="formDivA">
                <form>
                    <!-- Input Minimum Strip Width -->
                    <div class="input-group mb-3 input-group-sm">
                        <div class="input-group-prepend">
                            <span class="input-group-text"> Minimum Strip Width:</span>
                        </div>
                        <input type="number" class="form-control" id="minWidth" required>

                        <div class="input-group-append">
                            <span class="input-group-text"> mm </span>
                        </div>
                    </div>
                    <!-- Input Maximum Strip Width -->
                    <div class="input-group mb-3 input-group-sm">
                        <div class="input-group-prepend">
                            <span class="input-group-text"> Maximum Strip Width:</span>
                        </div>
                        <input type="number" class="form-control" id="maxWidth" placeholder="" required>
                        <div class="input-group-append">
                            <span class="input-group-text"> mm </span>
                        </div>
                    </div>
                </form>
            </div>

        </div>
        <!-- Input Maximum  CLD -->
        <!-- Input Maximum HOP -->
        <!-- Input Preferred Installation Height -->

        <div class="col-4 text-center">
            <div class="formDivA">
                <form>
                    <div class="input-group mb-3 input-group-sm">
                        <div class="input-group-prepend">
                            <span class="input-group-text"> Maximum  CLD:</span>
                        </div>
                        <input type="number" class="form-control" id="maxCLD" max="100" required  data-toggle="tooltip" data-placement="top" title="CLD max 100mm">
                        <div class="input-group-append">
                            <span class="input-group-text"> mm </span>
                        </div>
                    </div>

                    <div class="input-group mb-3 input-group-sm">
                        <div class="input-group-prepend">
                            <span class="input-group-text" id="basic-addon1">Maximum HOP:</span>
                        </div>
                        <input type="number" class="form-control" id="maxHOP" max="30" required  data-toggle="tooltip" data-placement="top" title="HOP max 30mm">
                        <div class="input-group-append">
                            <span class="input-group-text"> mm </span>
                        </div>
                    </div>

                    <div class="input-group mb-3 input-group-sm">
                        <div class="input-group-prepend">
                            <span class="input-group-text" id="basic-addon1" >Preferred Installation Height:</span>
                        </div>
                        <input type="number" class="form-control" id="PreferredHeight" max="1600" data-toggle="tooltip" data-placement="top" title="Leave Preferred Installation Height blank for new installation">
                        <div class="input-group-append">
                            <span class="input-group-text"> mm </span>
                        </div>
                    </div>


                </form>
            </div>


 
        </div>

        <div class="col-2 text-center">

        </div>

    </div>

    <!-- Button calculate -->
    <div class="row">


        <div class="col-6 text-center">

        </div>
        <div class="col-2 text-left">
            <button class="btn btn-primary btn-sm" type="submit" id="calculateButton"onclick="calculate();" data-toggle="tooltip" data-placement="top" title="">Calculate</button>
        </div>

        <div class="col-2 text-right">
            <br /> <h4 style="color: lightgrey;">Results</h4>

        </div>
    </div>


    <div class="row">
        <div class="col-2 text-center">
        </div>
        <div class="col-4 text-center">
            <div class="formDivB">
                <form>
                    <div class="input-group mb-3 input-group-sm">
                        <span class="border-left"></span>

                        <div class="input-group-prepend">
                            <label class="input-group-text" for="inputGroupSelect01">Scanner Orientation:</label>
                        </div>
                        <select class="custom-select" id="selOrientation">
                            <option value="" disabled selected>Choose</option>
                            <option value="LEFT">Left</option>
                            <option value="RIGHT">Right</option>
                        </select>
                    </div>

                    <div class="input-group mb-3 input-group-sm">
                        <div class="input-group-prepend">
                            <label class="input-group-text" for="inputGroupSelect02">Communication Protocol:</label>
                        </div>
                        <select class="custom-select" id="HostCommunicationProtocol" onchange="HCPfunction()">
                            <option value="TS-542">TS-542 TCP-IP</option>
                            <option value="TS-549">TS-549 ProfiBUS/ProfiNET</option>
                            <option value="TBD">TBD</option>
                        </select>

                    </div>
                </form>
            </div>
            <h3 style="color: cadetblue;">2.Scope of Supply</h3>

        </div>

        <div class="col-4 text-center">

            <div class="formDivC">
                <form>
                    <div class="input-group mb-3 input-group-sm">
                        <div class="input-group-prepend">
                            <span class="input-group-text">Installation Height:</span>
                        </div>
                        <input type="text" class="form-control" id="instHeight" placeholder="HEIGHT" max="1600" disabled>
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
                    <div class="input-group mb-3 input-group-sm">
                        <div class="input-group-prepend">
                            <span class="input-group-text">Lens Focus Length:</span>
                        </div>
                        <input type="text" class="form-control" id="lensFocus" placeholder="LENS" disabled>
                        <div class="input-group-append">
                            <span class="input-group-text">mm</span>
                        </div>
                    </div>
                </form>
            </div>

        </div>
        <div class="col-2 text-center">
        </div>
    </div>


    <div class="row">
        <div class="col-1 text-center">
        </div>
        <div class="col-5 text-center">
            <div class="formDivB">
                <form>
                    <div class="input-group mb-3 input-group-sm">

                        <div class="input-group-prepend">
                            <input type="checkbox" id="selProfiBusNet" disabled>
                            <label class="input-group-text" for="inputGroupSelect03">ProfiBUS/ProfiNet</label>
                        </div>
                        <select class="custom-select" id="selectedProfi" name="selectedProfi" disabled>

                            <option value="" disabled selected>Choose Type</option>
                            <option value="PB">ProfiBUS</option>
                            <option value="PN">ProfiNET</option>
                        </select>
                        <select class="custom-select" id="ProfiPS" name="ProfiPS" disabled>
                            <option value="" disabled selected>Power Supply</option>
                            <option value="DC">DC 24V</option>
                            <option value="AC">AC 110/220V</option>
                        </select>

                        <select class="custom-select" id="ProfiMC" name="ProfiMC" disabled>
                            <option value="">without M/C</option>
                            <option value="M">with 1 M/C</option>
                            <option value="MM">with 2 M/C</option>

                        </select>


                    </div>

                    <div class="input-group mb-3 input-group-sm">

                        <div class="input-group-prepend">
                            <input type="checkbox" id="selKIP" value="PL055640-1" name="KIP Software CD">
                            <label class="input-group-text" for="inputGroupSelect04">Operator's Station</label>
                        </div>

                        <select class="custom-select" id="selKIPQTY" name="selKIPQTY">
                            <option value="" disabled selected>QTY</option>
                            <option value="1">1</option>
                            <option value="2">2</option>
                            <option value="3">3</option>
                        </select>

                        <select class="custom-select" id="selectedPC" name="selectedPC">
                            <option value="1">KELK 1U PC</option>
                            <option value="2">KELK PC+M/C</option>
                            <option value="">KIP ONLY</option>
                        </select>


                    </div>
                    <div class="input-group mb-3 input-group-sm">

                        <div class="input-group-prepend">
                            <input type="checkbox" id="selDiscrete">
                            <label class="input-group-text" for="inputGroupSelect04">Discrete IO</label>
                        </div>

                        <select class="custom-select" id="DiscreteInput" name="DiscreteInput">
                            <option value="" disabled selected>Input</option>
                            <option value="V">+/-10V</option>
                            <option value="C">4-20mA</option>
                        </select>

                        <select class="custom-select" id="DiscreteOutput" name="DiscreteOutput">
                            <option value="" disabled selected>Output</option>
                            <option value="V">+/-10V</option>
                            <option value="C">4-20mA</option>
                        </select>
                        <select class="custom-select" id="DiscreteMC" name="DiscreteMC">
                            <option value="">without M/C</option>
                            <option value="M">with 1 M/C</option>
                        </select>


                    </div>
                </form>
            </div>
        </div>


        <div class="col-4 text-center">
            <div class="formDivC">
                <form>
                    <span class="input-group-text">Calculated Field of View</span>
                    <div class="input-group mb-3 input-group-sm">
                        <div class="input-group-prepend">
                            <span class="input-group-text">Material Range @max HOP:</span>

                            <input type="text" class="form-control" id="minFOVatHOP" placeholder="MIN" disabled>
                            <div class="input-group-append">
                                <span class="input-group-text">mm</span>
                            </div>
                            <input type="text" class="form-control" id="maxFOVatHOP" placeholder="MAX" disabled>
                            <div class="input-group-append">
                                <span class="input-group-text">mm</span>
                            </div>
                        </div>

                        <div class="input-group-prepend">
                            <span class="input-group-text"> Material Range  @Pass Line:</span>

                            <input type="text" class="form-control" id="minFOVPassline" placeholder="MIN" disabled>
                            <div class="input-group-append">
                                <span class="input-group-text">mm</span>
                            </div>
                            <input type="text" class="form-control" id="maxFOVPassline" placeholder="MAX" disabled>
                            <div class="input-group-append">
                                <span class="input-group-text">mm</span>
                            </div>
                        </div>

                    </div>
                </form>
            </div>


        </div>
        <div class="col-2 text-center">
        </div>
    </div>

    <div class="row">
        <div class="col-6 text-center">
            <button class="btn btn-primary btn-sm" type="submit" id="workorderButton" onclick="download_csv();"   data-toggle="tooltip" data-placement="top" title="" >Generate WorkOrder</button>
        </div>
        <div class="col-5 text-left">
            <button class="btn btn-info btn-sm" type="button" id="helpButton" color="green"  data-toggle="tooltip" data-placement="top" title="">HELP</button>
        </div>
    </div>
</body>
</html>


<script>
    var coll = document.getElementsByClassName("collapsible");
    var i;

    for (i = 0; i < coll.length; i++) {
        coll[i].addEventListener("click", function () {
            this.classList.toggle("active");
            var content = this.nextElementSibling;
            if (content.style.display === "block") {
                content.style.display = "none";
            } else {
                content.style.display = "block";
            }
        });
    }

    var Camber = 3.0;  // fixed camera camber angle
    var CCD = 28.672 * (2048 - 24) / 2048; //edges are not detected in the first and last 12 pixels of CCD.
    var viewingAngle;
    var angleAA;


    var minHeight = 900;
    var maxHeight = 1600;

    function validateHeight() {
        var element = document.getElementById("PreferredHeight");
        var vHeight = parseInt(element.value);
        if ((vHeight > maxHeight) || (vHeight < minHeight)) {
            document.getElementById("lensFocus").value = "test";

            element.style.color = "red";
        } else {

            element.style.color = "black";

        }

    }

    function HCPfunction() {
        if (document.getElementById("HostCommunicationProtocol").value != "TS-549") {
            document.getElementById("selProfiBusNet").disabled = true
            document.getElementById("selectedProfi").disabled = true
            document.getElementById("ProfiMC").disabled = true
            document.getElementById("ProfiPS").disabled = true
            document.getElementById("selProfiBusNet").checked = false

        } else {
            document.getElementById("selProfiBusNet").disabled = false 
            document.getElementById("selectedProfi").disabled = false
            document.getElementById("ProfiMC").disabled = false
            document.getElementById("ProfiPS").disabled = false
            document.getElementById("selProfiBusNet").checked = true

        }



    }

    var defaultCLD = 50;
    var defaultHOP = 10;
    var defaultminWidth = 700;
    var defaultmaxWidth = 1700;
    document.getElementById("maxCLD").value = defaultCLD;
    document.getElementById("maxHOP").value = defaultHOP;
    document.getElementById("minWidth").value = defaultminWidth;
    document.getElementById("maxWidth").value = defaultmaxWidth;
    document.getElementById("calculateButton").title ="1.Enter Centerline Deviation and Hop values. Note: CLD max = 100mm  and Hop max =30mm\n 2. For new installation leave the preferred Installation Height blank and press Calculate\n 3.For existing installation: Enter Preferred Installation Height (900-1600mm) and press Calculate"
    document.getElementById("workorderButton").title ="1.Choose Scanner Orientation\n2.Choose Communication Protocol\n3.Choose PrifiBus/ProfiNet\4.Choose HMI and IO options\n5. Click Generate Work Order\n6.Download Excel File" 

    document.getElementById("helpButton").title = '1. Enter Maximum and Minimum Material Width\n'
        + '2. Enter Centerline Deviation and Hop values.Note: CLD max = 100mm  and Hop max = 30mm\n'
        + '3.1 For new installation leave the Preferred Installation height blank.\n'
        + '3.2 For existing installations: Enter Preferred Installation Height note: limits(900-1600mm)\n'
        + '4. Click "Calculate" button to get design\n'
        + '5. Choose Scanner Orientation\n'
        + '6. Choose Communication Protocol\n'
        + '7. Choose HMI and IO options\n'
        +'8. Click "Generate Workorder" button to generate Work Order in Excel';



    var LensFocusLength;
    var RequiredCameraSeparation;
    var InstallationHeight;


 //   var PreferredHeight
    var KELKPC1U = ['', 'D1', '', 'EA', '*09117', '19\" RackMounted 1U Compute', ' ', 'PUR', ' ', ' ', ' ', ' ', '1']
    var Monitor = ['', 'D2', '', 'EA', '*08018', '22\" Monitor ', ' ', 'PUR', ' ', ' ', ' ', ' ', '1']
    var Keyboard = ['', 'D3', '', 'EA', '*08836', 'Keyboard ', ' ', 'PUR', ' ', ' ', ' ', ' ', '1']
    var Mouse = ['', 'D4', '', 'EA', '*08837', 'Mouse ', ' ', 'PUR', ' ', ' ', ' ', ' ', '1']
    var DesktopMC = ['', 'D5', '', 'EA', '*07446', '100M MultiMode Desktop Media Converotr with Power Supply', ' ', 'PUR', ' ', ' ', ' ', ' ', '1']
    var KIP = ['', 'D6', '', 'EA', 'PL055640-1', 'KELK Instrumentation Panel CD', ' ', 'MFG', ' ', ' ', ' ', ' ', '1']
    var DiscreteIO = ['', 'D6', '1', 'EA', 'PL059820', 'Accuband C775FF Discrete IO Assembly', ' ', 'MFG', ' ', ' ', ' ', ' ', '1']

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
    var C775ItemB= [
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
        ['1', 'D', '', 'EA', '', 'OPERATOR\'S INTERFACE', ' ', '', ' ', ' ', ' ', ' ', '']
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
 //       var sel = document.getElementById("selectedProfi");

 //       var inpObj = document.getElementById("minWidth");
 //       if (!inpObj.checkValidity()) {
 //           document.getElementById("PreferredHeight").value = inpObj.validationMessage;
 //           break;
 //       }

        
        
 //       document.getElementById("PreferredHeight").value = sel.options[sel.selectedIndex].text;
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
        if (InstallationHeight > maxHeight) {
            document.getElementById("instHeight").style.color = "red"
        } else {
            document.getElementById("instHeight").style.color = "black"
        }

        document.getElementById("lensFocus").value = LensFocusLength
        document.getElementById("instHeight").value = InstallationHeight
        document.getElementById("cameraSeparation").value = RequiredCameraSeparation

        cameraHeightaboveHOP = InstallationHeight - maxHOP
        cameraFOV = Math.round(getFOV(angleAA, cameraHeightaboveHOP, cameraSeparation))-1
        maxStripWidth = RequiredCameraSeparation + cameraFOV
        minStripWidth = RequiredCameraSeparation - cameraFOV
        document.getElementById("minFOVatHOP").value = minStripWidth
        document.getElementById("maxFOVatHOP").value = maxStripWidth

        cameraFOV = Math.round(getFOV(angleAA, InstallationHeight, cameraSeparation))-1
        maxStripWidth = Math.round(RequiredCameraSeparation + cameraFOV)
        minStripWidth = Math.round(RequiredCameraSeparation - cameraFOV)
        document.getElementById("minFOVPassline").value = minStripWidth
        document.getElementById("maxFOVPassline").value = maxStripWidth

    }


    function prepItemD() {
        C775ItemD = [
            ['1', 'D', '', 'EA', '', 'OPERATOR\'S INTERFACE', ' ', '', ' ', ' ', ' ', ' ', '']
        ];

        var qty = document.getElementById("selKIPQTY").value;
        if ((document.getElementById("selKIP").checked) && ((document.getElementById("selectedPC").value == 1) || (document.getElementById("selectedPC").value == 2))) {
            // add KELK PC
            KELKPC1U[0] = C775ItemD.length + 1
            KELKPC1U[2] = qty
            C775ItemD.push(KELKPC1U);
            console.log(C775ItemD);
            //add Monitor
            Monitor[0] = C775ItemD.length + 1
            Monitor[2] = qty
            C775ItemD.push(Monitor);
            console.log(C775ItemD);
            //add Keyboard
            Keyboard[0] = C775ItemD.length + 1
            Keyboard[2] = qty
            C775ItemD.push(Keyboard);
            console.log(C775ItemD);
            //add Mouse
            Mouse[0] = C775ItemD.length + 1
            Mouse[2] = qty
            C775ItemD.push(Mouse);
            console.log(C775ItemD);
        }
        if ((document.getElementById("selKIP").checked) && (document.getElementById("selectedPC").value == 2)) {
            //add Media Convertor
            DesktopMC[0] = C775ItemD.length + 1
            DesktopMC[2] = qty
            C775ItemD.push(DesktopMC);
            console.log(C775ItemD);
        }


        if (document.getElementById("selKIP").checked) {
            //add KIP
            KIP[0] = C775ItemD.length + 1;
            KIP[1] = "D" + C775ItemD.length;
            KIP[2] = qty;
            C775ItemD.push(KIP);
            console.log(C775ItemD);
        }
        LineItem[0] = C775ItemD.length + 1
        LineItem[1] = ''
        LineItem[2] = ''
        LineItem[3] = ''
        LineItem[4] = ''
        LineItem[5] = ''
        LineItem[7] = ''
        LineItem[12] = ''
        C775ItemD.push(LineItem.concat());
        console.log(C775ItemD)

    }

    function prepare_lineItems() {
        var selectedOption
        var sel //= document.getElementById("selectedProfi");
 //       document.getElementById("PreferredHeight").value = 0;


 //       document.getElementById("PreferredHeight").value = sel.options[sel.selectedIndex].text;
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
        if (document.getElementById("selDiscrete").checked) {
            DiscreteIO[0] = C775ItemB.length+1
            DiscreteIO[1] = "B" + C775ItemB.length
            DiscreteIO[4] = 'PL059820-' + document.getElementById("DiscreteInput").value + document.getElementById("DiscreteOutput").value + 'W' + document.getElementById("DiscreteMC").value;
            C775ItemB.push(DiscreteIO);
            console.log(C775ItemB)
        }

        // ProfiBus /Pronet options
        sel = document.getElementById("selectedProfi");
        if (document.getElementById("selProfiBusNet").checked)  {
            LineItem[0] = C775ItemB.length + 1
            LineItem[1] = "B" + C775ItemB.length
            LineItem[2] = '1'
            LineItem[3] = 'EA'
            LineItem[4] = 'PL059823-' + document.getElementById("ProfiPS").value + document.getElementById("selectedProfi").value  + document.getElementById("ProfiMC").value;
            LineItem[5] = 'Accuband C775FF ' + sel.options[sel.selectedIndex].text +' Assembly'
            LineItem[7] = 'MFG'
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
    
        prepItemD();


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




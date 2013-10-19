File-Uploader
=============

Simple Ajax uploader for single files with forms and drag and drop. Usus the Form Data API which limits the use to these browser: http://caniuse.com/xhr2

Use the following elements in your html:

<div class="formContainer">
    <button id="chooseFile" class="chooseFileBtn">Choose File</button>
    <p class="fileName">The name of the file comes here...</p>

    <div id="fU">
        <form id="fUForm" enctype="multipart/form-data">
            <input id="fUInput" type="file" name="file" />
        </form>
      
        <button id="fUpCancel" class="cancelBtn">Cancel</button>
        <div id="fUDragContainer" class="dragContainer" draggable="true">Drop file here</div>
    </div>
</div>

<script src="http://code.jquery.com/jquery-1.10.1.min.js"></script>
<script src="js/jquery.fileuploader.js"></script>
<script>
        var options = {
	            validFileFormats: ['image/png', 'image/jpg', 'image/jpeg'],
	            maximumFileSize: 0,
          		errorMessages: [
                      "File is to big",
          			"Forbidden file format",
          			"File name is not correct"
          		],
	            onUploadDone: handleUploadDone,
	            onError: handleError,
	            onUploadStart: handleStart,
	            onProgress: handleProgress,
	            onCancelUpload: handleCancel,
	            url: "/upload",
          		action: "POST",
          		formUpload: true,
          		dragUpload: true	
	        }

			$("#fU").fileUploader(options);
</script>

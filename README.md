File-Uploader
=============

Simple Ajax uploader for single files with forms and drag and drop. Usus the Form Data API which limits the use to these browser: http://caniuse.com/xhr2

Options
-------
- validFileFormats: Array (default [])
- maximumFileSize: Number in MB (default 0 = unlimited)
- errorMessages: Array with error message (default: [ "File is to big", "Forbidden file format","File name is not correct"]

Use the following elements in your html:

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

		

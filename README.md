# dataTablesSQLSRVSSP
ssp.class.php for dataTables SSP, but modified for SQL Server (SQLSRV)

/*********************** HOW TO USE ***********************/

See https://datatables.net/examples/data_sources/server_side.html for setting up dataTables SSP.
Drop file ssp.class.php in your project folder, rename the file if you're already using ssp.class.php for MySQL as I'm using the same name as the original file, in which case you'll need to change line 66 of the server side processing script example :

	require( 'ssp.class.php' );
	
Just replace ssp.class.php with the new name!

/*********************** EDITED LINES ***********************/

///////////////////////////////////////////

Line 397 - SQL CONNEXION (PDO)

	try {
		$db = @new PDO("sqlsrv:Server={$sql_details['host']};Database={$sql_details['db']}", "{$sql_details['user']}","{$sql_details['pass']}");
		$db->setAttribute( PDO::ATTR_ERRMODE, PDO::ERRMODE_EXCEPTION );
	}

///////////////////////////////////////////

Line 92 - SQL "LIMIT"

	$limit = "OFFSET ".intval($request['start'])." ROWS FETCH NEXT ".intval($request['length'])." ROWS ONLY";

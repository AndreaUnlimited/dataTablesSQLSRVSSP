# dataTablesSQLSRVSSP
ssp.class.php for dataTables SSP, but modified for SQL Server (SQLSRV)

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

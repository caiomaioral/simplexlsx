# SimpleXLSX class 0.7.1 (Official)

Parse and retrieve data from Excel XLSx files. MS Excel 2007 workbooks PHP reader

**Sergey Shuchkin** <sergey.shuchkin@gmail.com> 2010-2017

	Example 1:
	$xlsx = new SimpleXLSX('book.xlsx');
	print_r( $xlsx->rows() );
	
	Example 2: 
	$xlsx = new SimpleXLSX('book.xlsx');
	print_r( $xlsx->rowsEx() );
	
	Example 3: 
	$xlsx = new SimpleXLSX('book.xlsx');
	print_r( $xlsx->rows(2) ); // second worksheet
	
	Example 4.1:
	$xlsx = new SimpleXLSX('book.xlsx');
	print_r( $xlsx->sheetNames() ); // array( 1 => 'Sheet 1', 3 => 'Catalog' );
	
	Example 4.2:
	$xlsx = new SimpleXLSX('book.xlsx');	
	echo 'Sheet Name 2 = '.$xlsx->sheetName(2);
	
	Example 5:
	$xlsx = new SimpleXLSX('book.xlsx');
	if ($xslx->success())
		print_r( $xlsx->rows() );
	else
		echo 'xlsx error: '.$xslx->error();
	
	Example 6:
	$xslx = new SimpleXLSX( file_get_contents('http://www.example.com/example.xlsx'), true); // load data
	list($num_cols, $num_rows) = $xlsx->dimension(2);
	echo $xlsx->sheetName(2).':'.$num_cols.'x'.$num_rows;

##History
v0.7.1 (2017-03-29) License added<br/>
v0.6.11 (2016-07-27) fixed timestamp()<br />
v0.6.10 (2016-06-10) fixed search entries (UPPERCASE)<br />
v0.6.9 (2015-04-12) $xlsx->datetime_format to force dates out<br />
v0.6.8 (2013-10-13) fixed dimension() where 1 row only, fixed rowsEx() empty cells indexes (Daniel Stastka)<br />
v0.6.7 (2013-08-10) fixed unzip (mac), added $debug param to _constructor to display errors<br />
v0.6.6 (2013-06-03) +entryExists()<br />
v0.6.5 (2013-03-18) fixed sheetName()<br />
v0.6.4 (2013-03-13) rowsEx(), _parse(): fixed date column type & format detection<br />
v0.6.3 (2013-03-13) rowsEx(): fixed formulas, added date type 'd', added format 'format'<br />
					dimension(): fixed empty sheet dimension<br />
                    + sheetNames() - returns array( sheet_id => sheet_name, sheet_id2 => sheet_name2 ...)<br />
v0.6.2 (2012-10-04) fixed empty cells, rowsEx() returns type and formulas now<br />
v0.6.1 (2012-09-14) removed "raise exception" and fixed _unzip<br />
v0.6 (2012-09-13) success(), error(), __constructor( $filename, $is_data = false )<br />
v0.5.1 (2012-09-13) sheetName() fixed<br />
v0.5 (2012-09-12) sheetName()<br />
v0.4 sheets(), sheetsCount(), unixstamp( $excelDateTime )<br />
v0.3 - fixed empty cells (Gonzo patch)<br />


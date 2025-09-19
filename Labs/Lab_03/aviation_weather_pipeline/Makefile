.PHONY: all fetch analyze clean
all: analyze

fetch: 
	echo "Start fetch of METAR data" 
	./fetch_metars.sh 
	echo "Finish fetch. Data saved in raw_metars" 

analyze: fetch
	echo "Start analysis of METAR data" 
	./analyze_data.sh
	echo "Analysis finished. Report saved as weather_report.csv"
	echo "Pipeline completed successfully"

clean: 
	echo "Cleaning files" 
	rm -rf raw_metars/ weather_report.csv
	echo "Cleaning complete"

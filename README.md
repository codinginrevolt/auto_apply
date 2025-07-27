# auto_apply

<ol>
<li> Install Nominatim: https://nominatim.org/release-docs/latest/admin/Installation/
    
    a. `sudo apt install postgresql`
    b. `sudo apt install postgis`
    c. `sudo apt install osm2pgsql`
    d. `pip install -r requirements.txt `
    e. Create the web user for Nominatim:
        i. Switch to the postgres user:
            `sudo -i -u postgres`
        ii. Create the www-data user:
            `createuser www-data`
</li>
<li> Download the OSM data file (e.g., from Geofabrik) and import it
    
    a. e.g,`wget https://download.geofabrik.de/europe/germany/berlin-latest.osm.pbf`
    b. `nominatim import --osm-file <file_just_downloaded> --no-updates 2>&1 | tee setup.log `
</li>
</ol>

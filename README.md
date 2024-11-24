# bee6310_final_project

Sources:
- [NOAA Climate Indices: Monthly Atmospheric and Ocean Time Series](https://psl.noaa.gov/data/climateindices/list/)
- [NOAA Northern Hemisphere Teleconnection Patterns](https://www.cpc.ncep.noaa.gov/data/teledoc/telecontents.shtml)
- [NOAA gridded climate data](https://psl.noaa.gov/data/gridded/index.html)
- [Tool to extract monthly time series from gridded data](https://psl.noaa.gov/data/timeseries/)
- [IRI](https://iridl.ldeo.columbia.edu/SOURCES/.Indices/.CPC_Indices/.NHTI/?Set-Language=en)
data/raw files description:


- Eastern Pacific Oscillation (EPO) ?????
- North Pacific Oscillation (NPO) ?????

- Artic Oscillation (AO)
    - AO.csv header=None, sep="\t", columns: [year, month,value] source: https://www.cpc.ncep.noaa.gov/products/precip/CWlink/daily_ao_index/monthly.ao.index.b50.current.ascii
- North Atlantic Oscillation (NAO)
    - NAO.csv header=None, sep="\t", columns: [year, month,value] source: https://www.cpc.ncep.noaa.gov/products/precip/CWlink/pna/norm.nao.monthly.b5001.current.ascii
    - IRI_NAO.tsv  [months since 1960-01-01	unitless] missing data: -99.900002 source: https://iridl.ldeo.columbia.edu/SOURCES/.Indices/.CPC_Indices/.NHTI/?Set-Language=en
- PNA
    - PNA.csv header=None, sep="\t", columns: [year, month,value] source: https://www.cpc.ncep.noaa.gov/products/precip/CWlink/pna/norm.pna.monthly.b5001.current.ascii
    - IRI_PNA.tsv  [months since 1960-01-01	unitless] missing data: -99.900002 source: https://iridl.ldeo.columbia.edu/SOURCES/.Indices/.CPC_Indices/.NHTI/?Set-Language=en
- Greenland Blocking Index (GBI) GBI.csv header=None, sep=?, columns: [year jan feb ... dec], missing value = -99.00 source: https://psl.noaa.gov/gcos_wgsp/Timeseries/Data/gbi.mon.data
- West Pacific (WP) 
    - not working aparently https://www.cpc.ncep.noaa.gov/data/teledoc/wp.shtml
    - tele_index.csv (standardized using 1980-2010)  **column 5** [year, month, NAO, EA, WP, EP/NP, PNA, EA/WR, SCA, TNH, POL, PT, Expl. Var.] source: https://ftp.cpc.ncep.noaa.gov/wd52dg/data/indices/tele_index.nh)
    - IRI_WP.tsv [months since 1960-01-01	unitless] missing data: -99.900002 source: https://iridl.ldeo.columbia.edu/SOURCES/.Indices/.CPC_Indices/.NHTI/?Set-Language=en
- East Atlantic (EA) 
    - tele_index.csv (standardized using 1980-2010)  **column 4** [year, month, NAO, EA, WP, EP/NP, PNA, EA/WR, SCA, TNH, POL, PT, Expl. Var.] source: https://ftp.cpc.ncep.noaa.gov/wd52dg/data/indices/tele_index.nh
    - IRI_EA.tsv [months since 1960-01-01	unitless] missing data: -99.900002 source: https://iridl.ldeo.columbia.edu/SOURCES/.Indices/.CPC_Indices/.NHTI/?Set-Language=en
- East Pacific/North Pacific (EPNP) 
    - Alternative: tele_index.csv (standardized using 1980-2010)  **column 6** [year, month, NAO, EA, WP, EP/NP, PNA, EA/WR, SCA, TNH, POL, PT, Expl. Var.] source: https://ftp.cpc.ncep.noaa.gov/wd52dg/data/indices/tele_index.nh)
    - IRI_EPNP.tsv [months since 1960-01-01	unitless] missing data: -99.900002 source: https://iridl.ldeo.columbia.edu/SOURCES/.Indices/.CPC_Indices/.NHTI/?Set-Language=en
- East Atlantic/Western Russia (EAWR) 
    - Alternative: tele_index.csv (standardized using 1980-2010)  **column 8** [year, month, NAO, EA, WP, EP/NP, PNA, EA/WR, SCA, TNH, POL, PT, Expl. Var.] source: https://ftp.cpc.ncep.noaa.gov/wd52dg/data/indices/tele_index.nh
    - IRI_EAWR.tsv [months since 1960-01-01	unitless] missing data: -99.900002 source: https://iridl.ldeo.columbia.edu/SOURCES/.Indices/.CPC_Indices/.NHTI/?Set-Language=en
- Scandinavian (SCA) 
    - Alternative: tele_index.csv (standardized using 1980-2010)  **column 9** [year, month, NAO, EA, WP, EP/NP, PNA, EA/WR, SCA, TNH, POL, PT, Expl. Var.] source: https://ftp.cpc.ncep.noaa.gov/wd52dg/data/indices/tele_index.nh
    - IRI_SCA.tsv [months since 1960-01-01	unitless] missing data: -99.900002 source: https://iridl.ldeo.columbia.edu/SOURCES/.Indices/.CPC_Indices/.NHTI/?Set-Language=en
- Tropical Northern Hemisphere (TNH) 
    - Alternative: tele_index.csv (standardized using 1980-2010)  **column 10** [year, month, NAO, EA, WP, EP/NP, PNA, EA/WR, SCA, TNH, POL, PT, Expl. Var.] source: https://ftp.cpc.ncep.noaa.gov/wd52dg/data/indices/tele_index.nh
    - IRI_TNH.tsv [months since 1960-01-01	unitless] missing data: -99.900002 source: https://iridl.ldeo.columbia.edu/SOURCES/.Indices/.CPC_Indices/.NHTI/?Set-Language=en
- Polar Eurasian (POL) 
    - Alternative: tele_index.csv (standardized using 1980-2010)  **column 11** [year, month, NAO, EA, WP, EP/NP, PNA, EA/WR, SCA, TNH, POL, PT, Expl. Var.] source: https://ftp.cpc.ncep.noaa.gov/wd52dg/data/indices/tele_index.nh
    - IRI_POL.tsv [months since 1960-01-01	unitless] missing data: -99.900002 source: https://iridl.ldeo.columbia.edu/SOURCES/.Indices/.CPC_Indices/.NHTI/?Set-Language=en
- Ocean Nino Index (ONI, i.e. ENSO) ONI.csv header=None, sep=?, columns: [year jan feb ... dec], missing value = -99.00 source: https://psl.noaa.gov/data/correlation/oni.data
- Pacific Decadal Oscillation (PDO)
    - PDO.csv header=None, sep=?, columns: [year jan feb ... dec], missing value = -9.90 source: https://psl.noaa.gov/data/correlation/pdo.data (ends in mid 2022)
    - PDO_source_2.csv header: [time, PDO, index] normalized? source: https://oceanview.pfeg.noaa.gov/erddap/tabledap/cciea_OC_PDO.html
    - For complete series try the file sst.mnmean.nc from https://psl.noaa.gov/data/gridded/data.noaa.ersst.v5.html
- Atlantic Multi-decadal Oscillation (AMO) 
    - AMO.csv header=None, sep=?, columns: [year jan feb ... dec], missing value = -99.990 source: https://psl.noaa.gov/data/correlation/amon.us.long.data
- Quasi-biennial Oscillation (QBO) 
    - QBO.csv header=None, sep=?, columns: [year jan feb ... dec], missing value = -999.00  source: https://psl.noaa.gov/data/correlation/qbo.data
- Nino 1.2 
    - NINO_1_2.csv source: header=None, sep=?, columns: [year jan feb ... dec], missing value = -99.99 source: https://psl.noaa.gov/data/correlation/nina1.anom.data 
    - ersst5_nino.csv [YR   MON  NINO1_2  NINO1_2_ANOM   NINO3    NINO3_ANOM   NINO4    NINO4_ANOM   NINO3_4  NINO3_4_ANOM] source: https://www.cpc.ncep.noaa.gov/data/indices/ersst5.nino.mth.91-20.ascii
- Nino 4
     - NINO_4.csv source: header=None, sep=?, columns: [year jan feb ... dec], missing value = -99.99 source: https://psl.noaa.gov/data/correlation/nina4.anom.data 
    - ersst5_nino.csv [YR   MON  NINO1_2  NINO1_2_ANOM   NINO3    NINO3_ANOM   NINO4    NINO4_ANOM   NINO3_4  NINO3_4_ANOM] source: https://www.cpc.ncep.noaa.gov/data/indices/ersst5.nino.mth.91-20.ascii
---
swagger: "2.0"
x-collection-name: Washington Metropolitan Area Transit Authority
x-complete: 0
info:
  title: WMATA Rail Station Information XML - Path Between Stations
  description: "Description\r\n\r\nReturns a set of ordered stations and distances
    between two stations on the\r\nsame line.\r\n\r\nNote that this method is not
    suitable on its own as a pathfinding solution\r\nbetween stations.\r\n\r\nResponse
    Elements\r\n\r\n\r\n\r\n\r\nElement\r\n\r\nDescription\r\n\r\n\r\n\r\n\r\n\r\nPath\r\n\r\n\r\nArray
    containing path details (MetroPathItem)\r\n\r\n\r\n\r\n\r\n\r\n\r\nMetroPathItem\r\nElements\r\n\r\n\r\n\r\n\r\n\r\nDistanceToPrev\r\n\r\nDistance
    in feet to the previous station in the list.\r\n\r\n\r\n\r\nLineCode\r\n\r\nTwo-letter
    abbreviation for the line (e.g.: RD, BL, YL, OR, GR,\r\nor SV) this station's
    platform is on.\r\n\r\n\r\n\r\nSeqNum\r\n\r\nOrdered sequence number.\r\n\r\n\r\n\r\nStationCode\r\n\r\nStation
    code for this station. Use this value in other\r\nrail-related APIs to retrieve
    data about a station.\r\n\r\n\r\n\r\nStationName\r\n\r\nFull name for this station,
    as shown on the WMATA website."
  version: 1.0.0
host: api.wmata.com
basePath: /Rail.svc
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /json/BusIncidents:
    get:
      summary: JSON - Bus Incidents
      description: "Description\r\n\r\nReturns a set of reported bus incidents/delays
        for a given Route. Omit the\r\nRoute to return all reported items.\r\n\r\nNote
        that the Route parameter accepts only base route names and no\r\nvariations,
        i.e.: use 10A instead of 10Av1 and 10Av2.\r\n\r\nBus incidents/delays are
        refreshed once every 20 to 30 seconds approximately.\r\n\r\nResponse Elements\r\n\r\n\r\n\r\n\r\nElement\r\n\r\nDescription\r\n\r\n\r\n\r\n\r\n\r\nBusIncidents\r\n\r\n\r\nArray
        containing bus incident information (BusIncident).\r\n\r\n\r\n\r\n\r\n\r\n\r\nBusIncident\r\nElements\r\n\r\n\r\n\r\n\r\n\r\nDateUpdated\r\n\r\nDate
        and time (Eastern Standard Time) of last update. Will be\r\nin YYYY-MM-DDTHH:mm:ss
        format (e.g.: 2014-10-28T08:13:03).\r\n\r\n\r\n\r\nDescription\r\n\r\nFree-text
        description of the delay or incident.\r\n\r\n\r\n\r\nIncidentID\r\n\r\nUnique
        identifier for an incident.\r\n\r\n\r\n\r\nIncidentType\r\n\r\nFree-text description
        of the incident type. Usually\r\nDelay or Alert but is subject to change at
        any time.\r\n\r\n\r\n\r\nRoutesAffected\r\n\r\nArray containing routes affected.
        Routes listed are usually\r\nidentical to base route names (i.e.: not 10Av1
        or 10Av2, but 10A),\r\nbut may differ from what our bus methods return."
      operationId: 54763641281d830c946a3d75
      x-api-path-slug: jsonbusincidents-get
      parameters:
      - in: query
        name: Route
        description: Base bus route; variations are not recognized (i
      responses:
        200:
          description: OK
      tags:
      - Transit
      - Buses
      - Incidents
  /json/ElevatorIncidents:
    get:
      summary: JSON - Elevator/Escalator Outages
      description: "Description\r\n\r\nReturns a list of reported elevator and escalator
        outages at a\r\ngiven station. Omit the StationCode parameter to return all
        reported\r\noutages.\r\n\r\nNote that for stations with multiple platforms
        and therefore StationCodes\r\n(e.g.: Metro Center, L'Enfant Plaza, etc.),
        a distinct call is required for\r\neach StationCode.\r\n\r\nElevator and escalator
        outages are refreshed once every 20 to 30 seconds approximately.\r\n\r\nResponse
        Elements\r\n\r\n\r\n\r\n\r\nElement\r\n\r\nDescription\r\n\r\n\r\n\r\n\r\n\r\nElevatorIncidents\r\n\r\n\r\nArray
        containing elevator/escalator outage information\r\n(ElevatorIncident).\r\n\r\n\r\n\r\n\r\n\r\n\r\nElevatorIncident
        Elements\r\n\r\n\r\n\r\n\r\n\r\nDateOutOfServ\r\n\r\nDate and time (Eastern
        Standard Time) unit was reported out of\r\nservice. Will be in YYYY-MM-DDTHH:mm:ss
        format (e.g.:\r\n2014-10-27T15:17:00).\r\n\r\n\r\n\r\nDateUpdated\r\n\r\nDate
        and time (Eastern Standard Time) outage details was last\r\nupdated. Will
        be in YYYY-MM-DDTHH:mm:ss format (e.g.:\r\n2014-10-27T15:17:00).\r\n\r\n\r\n\r\nDisplayOrder\r\n\r\nDeprecated.\r\n\r\n\r\n\r\nLocationDescription\r\n\r\nFree-text
        description of the unit location within a station\r\n(e.g.: Escalator between
        mezzanine and\r\nplatform).\r\n\r\n\r\n\r\nStationCode\r\n\r\nUnit's station
        code. Use this value in other rail-related APIs\r\nto retrieve data about
        a station.\r\n\r\n\r\n\r\nStationName\r\n\r\nFull station name, may include
        entrance information (e.g.:\r\nMetro Center, G and 11th St\r\nEntrance).\r\n\r\n\r\n\r\nSymptomCode\r\n\r\nDeprecated.\r\n\r\n\r\n\r\nSymptomDescription\r\n\r\nDescription
        for why the unit is out of service or otherwise in\r\nreduced operation.\r\n\r\n\r\n\r\nTimeOutOfService\r\n\r\nDeprecated.
        Use the time\r\nportion of the DateOutOfServ element.\r\n\r\n\r\n\r\nUnitName\r\n\r\nUnique
        identifier for unit, by type (a single elevator and\r\nescalator may have
        the same UnitName, but no two elevators or two\r\nescalators will have the
        same UnitName).\r\n\r\n\r\n\r\nUnitStatus\r\n\r\nDeprecated. If listed here,\r\nthe
        unit is inoperational or otherwise impaired.\r\n\r\n\r\n\r\nUnitType\r\n\r\nType
        of unit. Will be ELEVATOR\r\nor ESCALATOR."
      operationId: 54763641281d830c946a3d76
      x-api-path-slug: jsonelevatorincidents-get
      parameters:
      - in: query
        name: StationCode
        description: Station code
      responses:
        200:
          description: OK
      tags:
      - Transit
      - Elevator
      - Incidents
  /json/Incidents:
    get:
      summary: JSON - Rail Incidents
      description: "Description\r\n\r\nReturns reported rail incidents (significant
        disruptions and delays to\r\nnormal service). The data is identical to WMATA's
        Metrorail Service Status\r\nfeed.\r\n\r\nRail incidents are refreshed once
        every 20 to 30 seconds approximately.\r\n\r\nResponse Elements\r\n\r\n\r\n\r\n\r\nElement\r\n\r\nDescription\r\n\r\n\r\n\r\n\r\n\r\nIncidents\r\n\r\n\r\nArray
        containing rail disruption information (Incident).\r\n\r\n\r\n\r\n\r\n\r\n\r\nIncident
        Elements\r\n\r\n\r\n\r\n\r\n\r\nDateUpdated\r\n\r\nDate and time (Eastern
        Standard Time) of last update. Will be\r\nin YYYY-MM-DDTHH:mm:SS format (e.g.:
        2010-07-29T14:21:28).\r\n\r\n\r\n\r\nDelaySeverity\r\n\r\nDeprecated.\r\n\r\n\r\n\r\nDescription\r\n\r\nFree-text
        description of the incident.\r\n\r\n\r\n\r\nEmergencyText\r\n\r\nDeprecated.\r\n\r\n\r\n\r\nEndLocationFullName\r\n\r\nDeprecated.\r\n\r\n\r\n\r\nIncidentID\r\n\r\nUnique
        identifier for an incident.\r\n\r\n\r\n\r\nIncidentType\r\n\r\nFree-text description
        of the incident type. Usually Delay or\r\nAlert but is subject to change at
        any time.\r\n\r\n\r\n\r\nLinesAffected\r\n\r\nSemi-colon and space separated
        list of line codes (e.g.:\r\nRD; or BL;\r\nOR; or BL; OR; RD;). We do\r\nplan
        to update this to return something more reasonable like an\r\narray, but until
        then, use code similar to the following:\r\n\r\n\"RD; GR; BL;\".split(/;[\\s]?/).filter(function(fn)
        { return fn\r\n!== ''; })\r\n\r\n\r\n\r\nPassengerDelay\r\n\r\nDeprecated.\r\n\r\n\r\n\r\n\r\nStartLocationFullName\r\n\r\nDeprecated."
      operationId: 54763641281d830c946a3d77
      x-api-path-slug: jsonincidents-get
      responses:
        200:
          description: OK
      tags:
      - Transit
      - Buses
      - Incidents
  /BusIncidents:
    get:
      summary: XML - Bus Incidents
      description: "Description\r\n\r\nReturns a set of reported bus incidents/delays
        for a given Route. Omit the\r\nRoute to return all reported items.\r\n\r\nNote
        that the Route parameter accepts only base route names and no\r\nvariations,
        i.e.: use 10A instead of 10Av1 and 10Av2.\r\n\r\nBus incidents/delays are
        refreshed once every 20 to 30 seconds approximately.\r\n\r\nResponse Elements\r\n\r\n\r\n\r\n\r\nElement\r\n\r\nDescription\r\n\r\n\r\n\r\n\r\n\r\nBusIncidents\r\n\r\n\r\nArray
        containing bus incident information (BusIncident).\r\n\r\n\r\n\r\n\r\n\r\n\r\nBusIncident\r\nElements\r\n\r\n\r\n\r\n\r\n\r\nDateUpdated\r\n\r\nDate
        and time (Eastern Standard Time) of last update. Will be\r\nin YYYY-MM-DDTHH:mm:ss
        format (e.g.: 2014-10-28T08:13:03).\r\n\r\n\r\n\r\nDescription\r\n\r\nFree-text
        description of the delay or incident.\r\n\r\n\r\n\r\nIncidentID\r\n\r\nUnique
        identifier for an incident.\r\n\r\n\r\n\r\nIncidentType\r\n\r\nFree-text description
        of the incident type. Usually\r\nDelay or Alert but is subject to change at
        any time.\r\n\r\n\r\n\r\nRoutesAffected\r\n\r\nArray containing routes affected.
        Routes listed are usually\r\nidentical to base route names (i.e.: not 10Av1
        or 10Av2, but 10A),\r\nbut may differ from what our bus methods return."
      operationId: 54763641281d830c946a3d78
      x-api-path-slug: busincidents-get
      parameters:
      - in: query
        name: Route
        description: Bus route
      responses:
        200:
          description: OK
      tags:
      - Transit
      - Buses
      - Incidents
  /ElevatorIncidents:
    get:
      summary: XML - Elevator/Escalator Outages
      description: "Description\r\n\r\nReturns a list of reported elevator and escalator
        outages at a\r\ngiven station. Omit the StationCode parameter to return all
        reported\r\noutages.\r\n\r\nNote that for stations with multiple platforms
        and therefore StationCodes\r\n(e.g.: Metro Center, L'Enfant Plaza, etc.),
        a distinct call is required for\r\neach StationCode.\r\n\r\nElevator and escalator
        outages are refreshed once every 20 to 30 seconds approximately.\r\n\r\nResponse
        Elements\r\n\r\n\r\n\r\n\r\nElement\r\n\r\nDescription\r\n\r\n\r\n\r\n\r\n\r\nElevatorIncidents\r\n\r\n\r\nArray
        containing elevator/escalator outage information\r\n(ElevatorIncident).\r\n\r\n\r\n\r\n\r\n\r\n\r\nElevatorIncident
        Elements\r\n\r\n\r\n\r\n\r\n\r\nDateOutOfServ\r\n\r\nDate and time (Eastern
        Standard Time) unit was reported out of\r\nservice. Will be in YYYY-MM-DDTHH:mm:ss
        format (e.g.:\r\n2014-10-27T15:17:00).\r\n\r\n\r\n\r\nDateUpdated\r\n\r\nDate
        and time (Eastern Standard Time) outage details was last\r\nupdated. Will
        be in YYYY-MM-DDTHH:mm:ss format (e.g.:\r\n2014-10-27T15:17:00).\r\n\r\n\r\n\r\nDisplayOrder\r\n\r\nDeprecated.\r\n\r\n\r\n\r\nLocationDescription\r\n\r\nFree-text
        description of the unit location within a station\r\n(e.g.: Escalator between
        mezzanine and\r\nplatform).\r\n\r\n\r\n\r\nStationCode\r\n\r\nUnit's station
        code. Use this value in other rail-related APIs\r\nto retrieve data about
        a station.\r\n\r\n\r\n\r\nStationName\r\n\r\nFull station name, may include
        entrance information (e.g.:\r\nMetro Center, G and 11th St\r\nEntrance).\r\n\r\n\r\n\r\nSymptomCode\r\n\r\nDeprecated.\r\n\r\n\r\n\r\nSymptomDescription\r\n\r\nDescription
        for why the unit is out of service or otherwise in\r\nreduced operation.\r\n\r\n\r\n\r\nTimeOutOfService\r\n\r\nDeprecated.
        Use the time\r\nportion of the DateOutOfServ element.\r\n\r\n\r\n\r\nUnitName\r\n\r\nUnique
        identifier for unit, by type (a single elevator and\r\nescalator may have
        the same UnitName, but no two elevators or two\r\nescalators will have the
        same UnitName).\r\n\r\n\r\n\r\nUnitStatus\r\n\r\nDeprecated. If listed here,\r\nthe
        unit is inoperational or otherwise impaired.\r\n\r\n\r\n\r\nUnitType\r\n\r\nType
        of unit. Will be ELEVATOR\r\nor ESCALATOR."
      operationId: 54763641281d830c946a3d79
      x-api-path-slug: elevatorincidents-get
      parameters:
      - in: query
        name: StationCode
        description: Two-letter station code
      responses:
        200:
          description: OK
      tags:
      - Transit
      - Elevator
      - Incidents
  /Incidents:
    get:
      summary: XML - Rail Incidents
      description: "Description\r\n\r\nReturns reported rail incidents (significant
        disruptions and delays to\r\nnormal service). The data is identical to WMATA's
        Metrorail Service Status\r\nfeed.\r\n\r\nRail incidents are refreshed once
        every 20 to 30 seconds approximately.\r\n\r\nResponse Elements\r\n\r\n\r\n\r\n\r\nElement\r\n\r\nDescription\r\n\r\n\r\n\r\n\r\n\r\nIncidents\r\n\r\n\r\nArray
        containing rail disruption information (Incident).\r\n\r\n\r\n\r\n\r\n\r\n\r\nIncident
        Elements\r\n\r\n\r\n\r\n\r\n\r\nDateUpdated\r\n\r\nDate and time (Eastern
        Standard Time) of last update. Will be\r\nin YYYY-MM-DDTHH:mm:SS format (e.g.:
        2010-07-29T14:21:28).\r\n\r\n\r\n\r\nDelaySeverity\r\n\r\nDeprecated.\r\n\r\n\r\n\r\nDescription\r\n\r\nFree-text
        description of the incident.\r\n\r\n\r\n\r\nEmergencyText\r\n\r\nDeprecated.\r\n\r\n\r\n\r\nEndLocationFullName\r\n\r\nDeprecated.\r\n\r\n\r\n\r\nIncidentID\r\n\r\nUnique
        identifier for an incident.\r\n\r\n\r\n\r\nIncidentType\r\n\r\nFree-text description
        of the incident type. Usually Delay or\r\nAlert but is subject to change at
        any time.\r\n\r\n\r\n\r\nLinesAffected\r\n\r\nSemi-colon and space separated
        list of line codes (e.g.:\r\nRD; or BL;\r\nOR; or BL; OR; RD;). We do\r\nplan
        to update this to return something more reasonable like an\r\narray, but until
        then, use code similar to the following:\r\n\r\n\"RD; GR; BL;\".split(/;[\\s]?/).filter(function(fn)
        { return fn\r\n!== ''; })\r\n\r\n\r\n\r\nPassengerDelay\r\n\r\nDeprecated.\r\n\r\n\r\n\r\n\r\nStartLocationFullName\r\n\r\nDeprecated."
      operationId: 54763641281d830c946a3d7a
      x-api-path-slug: incidents-get
      responses:
        200:
          description: OK
      tags:
      - Transit
      - Incidents
  /json/jLines:
    get:
      summary: JSON - Lines
      description: "Description\r\n\r\nReturns information about all rail lines.\r\n\r\nResponse
        Elements\r\n\r\n\r\n\r\n\r\nElement\r\n\r\nDescription\r\n\r\n\r\n\r\n\r\n\r\nLines\r\n\r\n\r\nArray
        containing line information (Line).\r\n\r\n\r\n\r\n\r\n\r\n\r\nLine Elements\r\n\r\n\r\n\r\n\r\n\r\nDisplayName\r\n\r\nFull
        name of line color.\r\n\r\n\r\n\r\nEndStationCode\r\n\r\nEnd station code.
        For example, will be E10 (Greenbelt) for the\r\nGreen Line, B11 (Glenmont)
        for the Red Line, etc. Use this value in\r\nother rail-related APIs to retrieve
        data about a station.\r\n\r\n\r\n\r\nInternalDestination1\r\n\r\nIntermediate
        terminal station code. During normal service, some\r\ntrains on some lines
        might end their trip prior to the\r\nStartStationCode or EndStationCode. A
        good example is on the Red\r\nLine where some trains stop at A11 (Grosvenor)
        or B08 (Silver\r\nSpring). Empty string if not defined.\r\n\r\n\r\n\r\nInternalDestination2\r\n\r\nSimilar
        to InternalDestination1.\r\n\r\n\r\n\r\nLineCode\r\n\r\nTwo-letter abbreviation
        for the line (e.g.: RD, BL, YL, OR, GR,\r\nor SV).\r\n\r\n\r\n\r\nStartStationCode\r\n\r\nStart
        station code. For example, will be F11 (Branch Avenue)\r\nfor the Green Line,
        A15 (Shady Grove) for the Red Line, etc. Use\r\nthis value in other rail-related
        APIs to retrieve data about a\r\nstation."
      operationId: getJsonJlines
      x-api-path-slug: jsonjlines-get
      responses:
        200:
          description: OK
      tags:
      - Transit
      - Lines
  /json/jStationParking:
    get:
      summary: JSON - Parking Information
      description: |-
        Description

        Returns parking information at a station based on a given StationCode. Omit
        the StationCode to return parking information for all stations.

        If a station has no parking, the StationsParking element will contain no
        child elements.

        Response Elements




        Element

        Description





        StationsParking


        Array containing station parking information (StationParking).






        StationParking
        Elements





        Code

        Station code. Useful when returning parking information for all
        stations. Use this value in other rail-related APIs to retrieve
        data about a station.



        Notes

        When not NULL, provides additional parking resources such as
        nearby lots.



        AllDayParking


        Structure describing all-day
        parking options.




        ShortTermParking


        Structure describing short-term
        parking options.






        AllDayParking
        Elements





        TotalCount

        Number of all-day parking spots available at a station.



        RiderCost

        All-day cost per day (weekday) for Metro riders. NULL when no all-day
        spots are available. For most stations, this value is identical to
        the NonRiderCost.

        For cases where the NonRiderCost is different, the lower cost per
        day requires a valid rail trip using a SmarTrip&reg; card
        originating from a station other than the one where the patron
        parked. To receive this lower rate, patrons must pay for their
        parking with the same SmarTrip&reg; card used to enter/exit
        Metrorail, and must exit the parking lot within two hours of
        exiting Metrorail.



        NonRiderCost

        All-day cost per day (weekday) for non-Metro riders. NULL when no all-day
        spots are available.





        ShortTermParking Elements





        SaturdayRiderCost

        Similar to RiderCost, except denoting Saturday prices.



        SaturdayNonRiderCost

        Similar to NonRiderCost, except denoting Saturday prices.



        TotalCount

        Number of short-term parking spots available at a station
        (parking meters).



        Notes

        Misc. information relating to short-term parking. NULL when no
        short-term spots are available.
      operationId: getJsonJstationparking
      x-api-path-slug: jsonjstationparking-get
      parameters:
      - in: query
        name: StationCode
        description: Station code
      responses:
        200:
          description: OK
      tags:
      - Transit
      - Stations
      - Parking
  /json/jPath:
    get:
      summary: JSON - Path Between Stations
      description: "Description\r\n\r\nReturns a set of ordered stations and distances
        between two stations on the\r\nsame line.\r\n\r\nNote that this method is
        not suitable on its own as a pathfinding solution\r\nbetween stations.\r\n\r\nResponse
        Elements\r\n\r\n\r\n\r\n\r\nElement\r\n\r\nDescription\r\n\r\n\r\n\r\n\r\n\r\nPath\r\n\r\n\r\nArray
        containing path details (MetroPathItem)\r\n\r\n\r\n\r\n\r\n\r\n\r\nMetroPathItem\r\nElements\r\n\r\n\r\n\r\n\r\n\r\nDistanceToPrev\r\n\r\nDistance
        in feet to the previous station in the list.\r\n\r\n\r\n\r\nLineCode\r\n\r\nTwo-letter
        abbreviation for the line (e.g.: RD, BL, YL, OR, GR,\r\nor SV) this station's
        platform is on.\r\n\r\n\r\n\r\nSeqNum\r\n\r\nOrdered sequence number.\r\n\r\n\r\n\r\nStationCode\r\n\r\nStation
        code for this station. Use this value in other\r\nrail-related APIs to retrieve
        data about a station.\r\n\r\n\r\n\r\nStationName\r\n\r\nFull name for this
        station, as shown on the WMATA website."
      operationId: getJsonJpath
      x-api-path-slug: jsonjpath-get
      parameters:
      - in: query
        name: FromStationCode
        description: Station code for the origin station
      - in: query
        name: ToStationCode
        description: Station code for the destination station
      responses:
        200:
          description: OK
      tags:
      - Transit
      - Paths
  /json/jStationEntrances:
    get:
      summary: JSON - Station Entrances
      description: "Description\r\n\r\nReturns a list of nearby station entrances
        based on latitude, longitude, and\r\nradius (meters). Omit search parameters
        to return all station entrances.\r\n\r\nResponse Elements\r\n\r\n\r\n\r\n\r\nElement\r\n\r\nDescription\r\n\r\n\r\n\r\n\r\n\r\nEntrances\r\n\r\n\r\nArray
        containing detailed information about station entrances\r\n(StationEntrance).\r\n\r\n\r\n\r\n\r\n\r\n\r\nStationEntrance
        Elements\r\n\r\n\r\n\r\n\r\n\r\nDescription\r\n\r\nAdditional information
        for the entrance, if available.\r\nCurrently available data usually shows
        the same value as the Name\r\nelement.\r\n\r\n\r\n\r\nID\r\n\r\nDeprecated.\r\n\r\n\r\n\r\nLat\r\n\r\nLatitude.\r\n\r\n\r\n\r\nLon\r\n\r\nLongitude.\r\n\r\n\r\n\r\nName\r\n\r\nName
        of the entrance (usually the station name and nearest\r\nintersection).\r\n\r\n\r\n\r\nStationCode1\r\n\r\nThe
        station code associated with this entrance. Use this value\r\nin other rail-related
        APIs to retrieve data about a station.\r\n\r\n\r\n\r\nStationCode2\r\n\r\nFor
        stations containing multiple platforms (e.g.: Gallery\r\nPlace, Fort Totten,
        L'Enfant Plaza, and Metro Center), the other\r\nstation code."
      operationId: getJsonJstationentrances
      x-api-path-slug: jsonjstationentrances-get
      parameters:
      - in: query
        name: Lat
        description: Center point Latitude, required if Longitude and Radius are specified
      - in: query
        name: Lon
        description: Center point Longitude, required if Latitude and Radius are specified
      - in: query
        name: Radius
        description: Radius (meters) to include in the search area, required if Latitude
          and Longitude are specified
      responses:
        200:
          description: OK
      tags:
      - Transit
      - Stations
      - Entrances
  /json/jStationInfo:
    get:
      summary: JSON - Station Information
      description: "Description\r\n\r\nReturns station location and address information
        based on a given\r\nStationCode.\r\n\r\nResponse Elements\r\n\r\n\r\n\r\n\r\nElement\r\n\r\nDescription\r\n\r\n\r\n\r\n\r\n\r\nAddress\r\n\r\n\r\nStructure
        describing address information.\r\n\r\n\r\n\r\n\r\nCode\r\n\r\nStation code.
        Repeated from input.\r\n\r\n\r\n\r\nLat\r\n\r\nLatitude.\r\n\r\n\r\n\r\nLineCode1\r\n\r\nTwo-letter
        abbreviation for the line (e.g.: RD, BL, YL, OR, GR,\r\nor SV) served by this
        station.\r\n\r\n\r\n\r\nLineCode2\r\n\r\nAdditional line served by this station.
        This is often the case\r\nwhen stations have multiple platforms (e.g.: Gallery
        Place, Fort\r\nTotten, L'Enfant Plaza, and Metro Center).\r\n\r\n\r\n\r\nLineCode3\r\n\r\nSimilar
        to function as LineCodeX.\r\n\r\n\r\n\r\nLineCode4\r\n\r\nSimilar to function
        as LineCodeX. Currently not in use.\r\n\r\n\r\n\r\nLon\r\n\r\nLongitude.\r\n\r\n\r\n\r\nName\r\n\r\nStation
        name.\r\n\r\n\r\n\r\nStationTogether1\r\n\r\nFor stations with multiple platforms
        (e.g.: Gallery Place, Fort\r\nTotten, L'Enfant Plaza, and Metro Center), the
        additional\r\nStationCode will be listed here.\r\n\r\n\r\n\r\nStationTogether2\r\n\r\nSimilar
        in function to StationTogether2. Currently not in\r\nuse.\r\n\r\n\r\n\r\n\r\n\r\nAddress
        Elements\r\n\r\n\r\n\r\n\r\n\r\nCity\r\n\r\nCity.\r\n\r\n\r\n\r\nState\r\n\r\nState
        (abbreviated).\r\n\r\n\r\n\r\nStreet\r\n\r\nStreet address (for GPS use).\r\n\r\n\r\n\r\nZip\r\n\r\nZip
        code."
      operationId: getJsonJstationinfo
      x-api-path-slug: jsonjstationinfo-get
      parameters:
      - in: query
        name: StationCode
        description: Station code
      responses:
        200:
          description: OK
      tags:
      - Transit
      - Stations
  /json/jStations:
    get:
      summary: JSON - Station List
      description: "Description\r\n\r\nReturns a list of station location and address
        information based on a given\r\nLineCode. Omit the LineCode to return all
        stations. The response is an array of\r\nobjects identical to those returned
        in the Station Information method.\r\n\r\nResponse Elements\r\n\r\n\r\n\r\n\r\nElement\r\n\r\nDescription\r\n\r\n\r\n\r\n\r\n\r\nStations\r\n\r\n\r\nArray
        containing station information (Station).\r\n\r\n\r\n\r\n\r\n\r\n\r\nStation
        Elements\r\n\r\n\r\n\r\n\r\n\r\nAddress\r\n\r\n\r\nStructure describing address
        information.\r\n\r\n\r\n\r\n\r\nCode\r\n\r\nStation code. Repeated from input.\r\n\r\n\r\n\r\nLat\r\n\r\nLatitude.\r\n\r\n\r\n\r\nLineCode1\r\n\r\nTwo-letter
        abbreviation for the line (e.g.: RD, BL, YL, OR, GR,\r\nor SV) served by this
        station.\r\n\r\n\r\n\r\nLineCode2\r\n\r\nAdditional line served by this station.
        This is often the case\r\nwhen stations have multiple platforms (e.g.: Gallery
        Place, Fort\r\nTotten, L'Enfant Plaza, and Metro Center).\r\n\r\n\r\n\r\nLineCode3\r\n\r\nSimilar
        to function as LineCodeX.\r\n\r\n\r\n\r\nLineCode4\r\n\r\nSimilar to function
        as LineCodeX. Currently not in use.\r\n\r\n\r\n\r\nLon\r\n\r\nLongitude.\r\n\r\n\r\n\r\nName\r\n\r\nStation
        name.\r\n\r\n\r\n\r\nStationTogether1\r\n\r\nFor stations with multiple platforms
        (e.g.: Gallery Place, Fort\r\nTotten, L'Enfant Plaza, and Metro Center), the
        additional\r\nStationCode will be listed here.\r\n\r\n\r\n\r\nStationTogether2\r\n\r\nSimilar
        in function to StationTogether2. Currently not in\r\nuse.\r\n\r\n\r\n\r\n\r\n\r\nAddress
        Elements\r\n\r\n\r\n\r\n\r\n\r\nCity\r\n\r\nCity.\r\n\r\n\r\n\r\nState\r\n\r\nState
        (abbreviated).\r\n\r\n\r\n\r\nStreet\r\n\r\nStreet address (for GPS use).\r\n\r\n\r\n\r\nZip\r\n\r\nZip
        code."
      operationId: getJsonJstations
      x-api-path-slug: jsonjstations-get
      parameters:
      - in: query
        name: LineCode
        description: Two-letter line code abbreviation:RD - RedYL - YellowGR - GreenBL
          - BlueOR - OrangeSV - Silver
      responses:
        200:
          description: OK
      tags:
      - Transit
      - Stations
  /json/jStationTimes:
    get:
      summary: JSON - Station Timings
      description: "Description\r\n\r\nReturns opening and scheduled first/last train
        times based on a given\r\nStationCode. Omit the StationCode to return timing
        information for all\r\nstations.\r\n\r\nNote that for stations with multiple
        platforms (e.g.: Metro Center, L'Enfant\r\nPlaza, etc.), a distinct call is
        required for each StationCode to retrieve the\r\nfull set of train times at
        such stations.\r\n\r\nResponse Elements\r\n\r\n\r\n\r\n\r\nElement\r\n\r\nDescription\r\n\r\n\r\n\r\n\r\n\r\nStationTimes\r\n\r\n\r\nArray
        containing station timing information (StationTime).\r\n\r\n\r\n\r\n\r\n\r\n\r\nStationTime\r\nElements\r\n\r\n\r\n\r\n\r\n\r\nCode\r\n\r\nStation
        code for this station. Use this value in other\r\nrail-related APIs to retrieve
        data about a station.\r\n\r\n\r\n\r\nStationName\r\n\r\nFull name of the station.\r\n\r\n\r\n\r\n*Day
        Elements\r\n\r\n\r\nContainer elements containing timing information based
        on\r\nday of the week.\r\n\r\n\r\n\r\n\r\n\r\n\r\nMonday/Tuesday/Wednesday/etc.\r\nElements\r\n\r\n\r\n\r\n\r\n\r\nOpeningTime\r\n\r\nStation
        opening time. Format is HH:mm.\r\n\r\n\r\n\r\nFirstTrains\r\n\r\n\r\nStructure
        containing first train\r\ninformation.\r\n\r\n\r\n\r\n\r\nLastTrains\r\n\r\n\r\nStructure
        containing last train\r\ninformation.\r\n\r\n\r\n\r\n\r\n\r\n\r\nFirstTrains
        Elements\r\n\r\n\r\n\r\n\r\n\r\nTime\r\n\r\nFirst train leaves the station
        at this time. Format is\r\nHH:mm.\r\n\r\n\r\n\r\nDestinationStation\r\n\r\nStation
        code for the train's destination. Use this value in\r\nother rail-related
        APIs to retrieve data about a station.\r\n\r\n\r\n\r\n\r\n\r\nLastTrains Elements\r\n\r\n\r\n\r\n\r\n\r\nTime\r\n\r\nLast
        train leaves the station at this time. Format is HH:mm.\r\nNote that when
        the time is AM, it signifies the next day. For\r\nexample, a value of 02:30
        under a Saturday element means the last\r\ntrain leaves on Sunday at 2:30
        AM.\r\n\r\n\r\n\r\nDestinationStation\r\n\r\nStation code for the train's
        destination. Use this value in\r\nother rail-related APIs to retrieve data
        about a station."
      operationId: getJsonJstationtimes
      x-api-path-slug: jsonjstationtimes-get
      parameters:
      - in: query
        name: StationCode
        description: Station code
      responses:
        200:
          description: OK
      tags:
      - Transit
      - Stations
      - Times
  /json/jSrcStationToDstStationInfo:
    get:
      summary: JSON - Station to Station Information
      description: "Description\r\n\r\nReturns a distance, fare information, and estimated
        travel time between any\r\ntwo stations, including those on different lines.
        Omit both parameters to\r\nretrieve data for all stations.\r\n\r\nResponse
        Elements\r\n\r\n\r\n\r\n\r\nElement\r\n\r\nDescription\r\n\r\n\r\n\r\n\r\n\r\nStationToStationInfos\r\n\r\n\r\nArray
        containing station to station information (StationToStationInfo).\r\n\r\n\r\n\r\n\r\n\r\n\r\nStationToStationInfo
        Elements\r\n\r\n\r\n\r\n\r\n\r\nCompositeMiles\r\n\r\nDistance in miles from
        the source to destination station.\r\n\r\n\r\n\r\nDestinationStation\r\n\r\nDestination
        station code. Use this value in other rail-related\r\nAPIs to retrieve data
        about a station.\r\n\r\n\r\n\r\nRailFare\r\n\r\n\r\nStructure containing fare
        information.\r\n\r\n\r\n\r\n\r\nRailTime\r\n\r\nEstimated travel time (schedule
        time) in minutes between the source and\r\ndestination station. This is not
        correlated to minutes (Min) in Real-Time Rail Predictions.\r\n\r\n\r\n\r\nSourceStation\r\n\r\nOrigin
        station code. Use this value in other rail-related APIs\r\nto retrieve data
        about a station.\r\n\r\n\r\n\r\n\r\n\r\nRailFare Elements\r\n\r\n\r\n\r\n\r\n\r\nOffPeakTime\r\n\r\nFare
        during off-peak times (times other than the ones described\r\nbelow).\r\n\r\n\r\n\r\nPeakTime\r\n\r\nFare
        during peak times (weekdays from opening to 9:30 AM and\r\n3-7 PM, and weekends
        from midnight to closing).\r\n\r\n\r\n\r\nSeniorDisabled\r\n\r\n\r\nReduced
        fare for senior citizens or\r\npeople with disabilities."
      operationId: getJsonJsrcstationtodststationinfo
      x-api-path-slug: jsonjsrcstationtodststationinfo-get
      parameters:
      - in: query
        name: FromStationCode
        description: Station code for the origin station
      - in: query
        name: ToStationCode
        description: Station code for the destination station
      responses:
        200:
          description: OK
      tags:
      - Transit
      - Stations
  /Lines:
    get:
      summary: XML - Lines
      description: "Description\r\n\r\nReturns information about all rail lines.\r\n\r\nResponse
        Elements\r\n\r\n\r\n\r\n\r\nElement\r\n\r\nDescription\r\n\r\n\r\n\r\n\r\n\r\nLines\r\n\r\n\r\nArray
        containing line information (Line).\r\n\r\n\r\n\r\n\r\n\r\n\r\nLine Elements\r\n\r\n\r\n\r\n\r\n\r\nDisplayName\r\n\r\nFull
        name of line color.\r\n\r\n\r\n\r\nEndStationCode\r\n\r\nEnd station code.
        For example, will be E10 (Greenbelt) for the\r\nGreen Line, B11 (Glenmont)
        for the Red Line, etc. Use this value in\r\nother rail-related APIs to retrieve
        data about a station.\r\n\r\n\r\n\r\nInternalDestination1\r\n\r\nIntermediate
        terminal station code. During normal service, some\r\ntrains on some lines
        might end their trip prior to the\r\nStartStationCode or EndStationCode. A
        good example is on the Red\r\nLine where some trains stop at A11 (Grosvenor)
        or B08 (Silver\r\nSpring). Empty string if not defined.\r\n\r\n\r\n\r\nInternalDestination2\r\n\r\nSimilar
        to InternalDestination1.\r\n\r\n\r\n\r\nLineCode\r\n\r\nTwo-letter abbreviation
        for the line (e.g.: RD, BL, YL, OR, GR,\r\nor SV).\r\n\r\n\r\n\r\nStartStationCode\r\n\r\nStart
        station code. For example, will be F11 (Branch Avenue)\r\nfor the Green Line,
        A15 (Shady Grove) for the Red Line, etc. Use\r\nthis value in other rail-related
        APIs to retrieve data about a\r\nstation."
      operationId: getLines
      x-api-path-slug: lines-get
      responses:
        200:
          description: OK
      tags:
      - Transit
      - Lines
  /StationParking:
    get:
      summary: XML - Parking Information
      description: |-
        Description

        Returns parking information at a station based on a given StationCode. Omit
        the StationCode to return parking information for all stations.

        If a station has no parking, the StationsParking element will contain no
        child elements.

        Response Elements




        Element

        Description





        StationsParking


        Array containing station parking information (StationParking).






        StationParking
        Elements





        Code

        Station code. Useful when returning parking information for all
        stations. Use this value in other rail-related APIs to retrieve
        data about a station.



        Notes

        When not NULL, provides additional parking resources such as
        nearby lots.



        AllDayParking


        Structure describing all-day
        parking options.




        ShortTermParking


        Structure describing short-term
        parking options.






        AllDayParking
        Elements





        TotalCount

        Number of all-day parking spots available at a station.



        RiderCost

        All-day cost per day (weekday) for Metro riders. NULL when no all-day
        spots are available. For most stations, this value is identical to
        the NonRiderCost.

        For cases where the NonRiderCost is different, the lower cost per
        day requires a valid rail trip using a SmarTrip&reg; card
        originating from a station other than the one where the patron
        parked. To receive this lower rate, patrons must pay for their
        parking with the same SmarTrip&reg; card used to enter/exit
        Metrorail, and must exit the parking lot within two hours of
        exiting Metrorail.



        NonRiderCost

        All-day cost per day (weekday) for non-Metro riders. NULL when no all-day
        spots are available.





        ShortTermParking Elements





        SaturdayRiderCost

        Similar to RiderCost, except denoting Saturday prices.



        SaturdayNonRiderCost

        Similar to NonRiderCost, except denoting Saturday prices.



        TotalCount

        Number of short-term parking spots available at a station
        (parking meters).



        Notes

        Misc. information relating to short-term parking. NULL when no
        short-term spots are available.
      operationId: getStationparking
      x-api-path-slug: stationparking-get
      parameters:
      - in: query
        name: StationCode
        description: Station code
      responses:
        200:
          description: OK
      tags:
      - Transit
      - Stations
      - Parking
  /Path:
    get:
      summary: XML - Path Between Stations
      description: "Description\r\n\r\nReturns a set of ordered stations and distances
        between two stations on the\r\nsame line.\r\n\r\nNote that this method is
        not suitable on its own as a pathfinding solution\r\nbetween stations.\r\n\r\nResponse
        Elements\r\n\r\n\r\n\r\n\r\nElement\r\n\r\nDescription\r\n\r\n\r\n\r\n\r\n\r\nPath\r\n\r\n\r\nArray
        containing path details (MetroPathItem)\r\n\r\n\r\n\r\n\r\n\r\n\r\nMetroPathItem\r\nElements\r\n\r\n\r\n\r\n\r\n\r\nDistanceToPrev\r\n\r\nDistance
        in feet to the previous station in the list.\r\n\r\n\r\n\r\nLineCode\r\n\r\nTwo-letter
        abbreviation for the line (e.g.: RD, BL, YL, OR, GR,\r\nor SV) this station's
        platform is on.\r\n\r\n\r\n\r\nSeqNum\r\n\r\nOrdered sequence number.\r\n\r\n\r\n\r\nStationCode\r\n\r\nStation
        code for this station. Use this value in other\r\nrail-related APIs to retrieve
        data about a station.\r\n\r\n\r\n\r\nStationName\r\n\r\nFull name for this
        station, as shown on the WMATA website."
      operationId: getPath
      x-api-path-slug: path-get
      parameters:
      - in: query
        name: FromStationCode
        description: Station code for the origin station
      - in: query
        name: ToStationCode
        description: Station code for the origin station
      responses:
        200:
          description: OK
      tags:
      - Transit
      - Paths
x-streamrank:
  polling_total_time_average: 0
  polling_size_download_average: 0
  streaming_total_time_average: 0
  streaming_size_download_average: 0
  change_yes: 0
  change_no: 0
  time_percentage: 0
  size_percentage: 0
  change_percentage: 0
  last_run: ""
  days_run: 0
  minute_run: 0
---
# WEST
Water Energy Simulation Toolset

*This project is not currently supported by Idaho National Laboratory as production grade software but is being made available to the public. Please use at your own risk.*

The Water-Energy Simulation Toolset (WEST) is an interactive simulation model that helps visualize impacts of different stakeholders on water quantity and quality of a watershed. This model is implemented in Powersim (http://www.powersim.com/) and requires Powersim in order to run. The case study is applied for the Snake River Basin with the fictional name Cutthroat River Basin. There are four groups of stakeholders of interest: hydropower, agriculture, flood control, and environmental protection. Users can easily interact with the model by changing certain inputs (climate change, fertilizer inputs, etc.) to observe the change over the entire system. Users can also change certain parameters to test their management policy.

There are 6 main components in WEST: reservoir, agriculture, hydropower, groundwater, nitrogen and phosphorus.

1. Reservoir
There are three major reservoirs in the Cutthroat River Basin. The Barley Falls Reservoir serves agricultural needs and provides flood control for the Barley Falls watershed using its 1.2 MAF of storage. The larger Open Plains reservoir is used primarily for agricultural supply and for backup flood control, with 1.73 MAF of usable storage. The Deep Canyon reservoir is operated primarily for hydropower generation and secondarily for flood control and downstream environmental needs. Its capacity is 1.43 MAF.

2. Agriculture
There are 3 major agricultural zones: Barley Falls, Open Plains and Bustling City. While both Barley Falls and Open Plains use surface and ground water within the Cutthroat Basin, Bustling City uses groundwater elsewhere. 

3. Hydropower
IPC (Independent Power Company) owns and manages hydropower generation from two major dams on the Cutthroat River. The first, at Open Plains reservoir, is heavily constrained because IPC only owns the turbines, not the dam. Open Plains turbines have a capacity of 100 MW and an average generation of 50 MW. The second, at Deep Canyon Complex, is the region's number one generator of electricity, with a capacity of nearly 1200 MW and a long-term average generation of about 600 MW. The Deep Canyon Complex consists of one storage dam that regulates two lower run-of-river impoundments. This complex is managed to maximize power generation when wholesale electricity prices are high, but it is also managed for environmental flows and flood control.

4. Groundwater
The Cutthroat Aquifer is a major water "source" for the region, comprising millions of acre-feet of storage for the Cutthroat Basin. This aquifer is intimately connected with surface flows in the basin, as indicated by the significant flow at Barley Springs and King Springs. In WEST, the aquifer is divided into Upper and Lower aquifers.

5. Nitrogen
Nitrogen is treated in the WEST model as a module, connecting to the existing WEST components through stream flows, ground water seepage rate, total irrigated area of each sub-watershed, reservoir volume, and aquifer volume. The component structure of WEST is maintained in the Nitrogen module by having separate components for Nitrogen in soil, ground water, reservoir and stream. 
The major pathway of Nitrogen in the Snake River Basin is through groundwater. For Barley Falls watershed, nitrogen from fertilizer application seeps to the Upper Aquifer. Part of this nitrogen will return to Barley Falls soil through groundwater irrigation. As the Upper Aquifer feeds the Barley Spring stream, nitrogen will emerge to the surface through this stream, then flows into the Open Plains Reservoir. Every time the dam gate is open for flood control, nitrogen from the reservoir flows downstream. 

The same mechanism applies for Open Plains soil. Nitrogen from fertilizers seeps to the Lower Aquifer and part of it returns to soil through ground water irrigation. For the Lower Aquifer, it receives nitrogen not only from the soil, but also from the Upper Aquifer. In this part of the watershed, nitrogen in groundwater emerges to the surface through King Spring, and then feeds into the Open Plains stream above Bustling City. Since farmers also use surface water of this stream to irrigate their crops, the second source of nitrogen entering Open Plains soil is through this pathway. 
Bustling City is a special case in the WEST model. Local farmers use surface water from local stream, but they also use ground water from another aquifer outside the model boundary. As a result, nitrogen from farming activities does not affect local groundwater. The only nitrogen source from water is through surface water. Going downstream from Open Plains to Bustling City, nitrogen reaches Deep Canyon Reservoir before leaving the system through dam operation.  
Land use is an important input to water quality of the model. In each farming region, four to five most common crops are selected. Crop types considered for Barley Falls include alfalfa, barley, potatoes, and wheat. Alfalfa, barley, corn, sugar beets and wheat are major crops in Open Plains. Bustling City crops include alfalfa, corn, sugar beets and wheat.

6. Phosphorus is treated in the WEST model as a module, connecting to the existing WEST components through stream flows, total irrigated area of each sub-watershed, reservoir volume, aquifer volume, crop types, irrigation timing, and weather information such as air temperature and precipitation. The component structure of WEST is maintained in the Phosphorus module by having separate components for Phosphorus in soil, ground water, reservoir, and stream. 
Phosphorus pathways in the environment are complex. For sub-watersheds with agriculture such as Barley Falls, Open Plains and Bustling City, phosphorus from fertilizers leaves soil in both soluble form and particles. The pathways include surface water runoff, water sediment, windborne sediment, and ground water leachate. Phosphorus in water returns to soil through both surface and ground water irrigation, except for Bustling City where ground water comes from another watershed. Phosphorus in ground water and surface water interacts where ground water feeds into stream such as Upper Aquifer feeding Barley Springs and Lower Aquifer feeding King Springs.
 

### Other Software
Idaho National Laboratory is a cutting edge research facility which is a constantly producing high quality research and software. Feel free to take a look at our other software and scientific offerings at:

[Primary Technology Offerings Page](https://www.inl.gov/inl-initiatives/technology-deployment)
[Supported Open Source Software](https://github.com/idaholab)
[Raw Experiment Open Source Software](https://github.com/IdahoLabResearch)
[Unsupported Open Source Software](https://github.com/IdahoLabCuttingBoard)

## Using The Simulation

The PowerSim file is split into smaller files via the unix "split" command as so:

`split -b 99m WEST.sip WEST.sip.`

You must rejoin these files to recreate the full simulation binary in order to run the simulation:

`cat WEST.sip.* > WEST.sip`

### License
Copyright 2017 Battelle Energy Alliance, LLC

This library is free software; you can redistribute it and/or
modify it under the terms of the GNU Lesser General Public
License as published by the Free Software Foundation; either
version 2.1 of the License, or (at your option) any later version.

This library is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the GNU
Lesser General Public License for more details.

You should have received a copy of the GNU Lesser General Public
License along with this library; if not, write to the Free Software
Foundation, Inc., 51 Franklin Street, Fifth Floor, Boston, MA  02110-1301  USA

Contact information of authors:
1. Ruby Nguyen: ruby.nguyen@inl.gov
Idaho National Laboratory, P.O. Box 1625, MS 3710, Idaho Falls, ID 83415 
2. Robert F. Jeffers: rfjeffe@sandia.gov
Sandia National Laboratories, P: (505) 845-8051

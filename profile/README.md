# Welcome to xLandscape

xLandscape is a modular framework for building models that simulate real-world landscape processes. Its core focuses on spatiotemporally explicit modeling using geoinformation, enabling simulations of patterns in landscapes through a Monte Carlo approach. With a modular design based on Component-Based Software Engineering (CBSE), xLandscape integrates various components to create flexible, open-source models for diverse applications.

## Software Architecture

xLandscape's software architecture is based on Component-Based Software Engineering (CBSE), featuring a modular design where individual modules, called components, provide specific functionalities. At its core, xLandscape operates as a microkernel, handling key landscape modeling functionalities and ensuring data consistency through semantics. Components interact with the core via a wrapper, enabling integration of external components. Components can be composed into models, which represent executable modeling software. The framework supports spatiotemporally explicit modeling, uses a Monte Carlo approach for variability propagation, and is designed to be scalable and adaptable to diverse modeling needs.

<img src="../img/xAquatic.png" alt="XAquatic" width="800"/>  

*Illustration of a model composition using the xLandscape framework. The ***core*** is represented by the framing 'L' (dark blue). The boxes represent **components** (eg, 'xDrift') of specific functionality. The composition make a model, here [xAquaticRisk](https://github.com/xlandscape/xAquaticRisk) which simulates pesticide use in catchments, exposure of streams, pesticide transport and fate in streams, as well as effects to aquatic invertebrate species. The integration assures inner consistancy of data and semantics (indicated by the light blue backgroud).*

## Applications in Ecotoxicology

xLandscape has been used to simulate the transport of chemical plant protection products from agronomic applications in crop fields to surface water streams ([xAquaticRisk](https://github.com/xlandscape/xAquaticRisk) and off-field soil ([xOffFieldSoilRisk](https://github.com/xlandscape/xOffFieldSoilRisk) for landscape-level scenarios using established e-fate simulation software. The results have been published in peer-reviewed academic journals, such as [here](https://pubs.acs.org/doi/10.1021/acs.est.3c02716) and [here](https://academic.oup.com/ieam/article/20/1/263/7725049).

While the main purpose of most modules is to create data using a Monte-Carlo approach, all results can easily be used for downstream analysis or visualization, as demonstrated in this short video:

https://github.com/user-attachments/assets/79eb0d36-8600-4cf4-a78c-5f14444f3122

## Components
Components implement a specific function of arbitrary complexity. They can be implemented natively or wrap external software. Components are not supposed to be executable but can be used to create models.

The following components have been implemented or are in development:

- [CascadeToxswa-Component](https://github.com/xlandscape/CascadeToxswa-Component) (Version: 2.3.7)  
- [CmfContinuous-Component](https://github.com/xlandscape/CmfContinuous-Component) (Version: 2.0.19)  
- [LEffectModel-Component](https://github.com/xlandscape/LEffectModel-Component) (Version: 2.1.6)  
- [LP50-Component](https://github.com/xlandscape/LP50-Component) (Version: 2.2.10)  
- [RunOffPrzm-Component](https://github.com/xlandscape/RunOffPrzm-Component) (Version: 2.1. 0)  
- [StepsRiverNetwork-Component](https://github.com/xlandscape/StepsRiverNetwork-Component) (Version: 2.1.8)  
- [StreamCom-Component](https://github.com/xlandscape/StreamCom-Component) (Version: 2.3.2)  
- [XSprayDrift-Component](https://github.com/xlandscape/XSprayDrift-Component) (Version: 2.5.6)  
- [Pearl-Component](https://github.com/xlandscape/Pearl-Component) (Version: No tags)  
- [CropProtection-Component](https://github.com/xlandscape/CropProtection-Component) (Version: 1.18.0)  
 Description: CropProtection is a Landscape Model component for simulating applications of plant protection products on fields within a given landscape

## Scenarios
Scenarios describe the (typically geographical) context in which models run to simulate, for example, the fate of pesticides. It is typically comprised of *environmental conditions* (abiotic, biotic, land cover, ...) of a particular region of interest. The following scenarios are currently available:

- [Scenario-GroteKemmelbeekTDI](https://github.com/xlandscape/Scenario-GroteKemmelbeekTDI) (Version: 1.8)  
- [Scenario-NRW1](https://github.com/xlandscape/Scenario-NRW1) (Version: 3.0)  
- [Scenario-NRW2](https://github.com/xlandscape/Scenario-NRW2) (Version: 3.0)  
- [Scenario-NRW3](https://github.com/xlandscape/Scenario-NRW3) (Version: 3.0)  
- [Scenario-OudebeekBeek7TDI](https://github.com/xlandscape/Scenario-OudebeekBeek7TDI) (Version: 3.21)  
- [Scenario-OudebeekTDI](https://github.com/xlandscape/Scenario-OudebeekTDI) (Version: 3.12)  
- [Scenario-Rummen](https://github.com/xlandscape/Scenario-Rummen) (Version: 2.12)  
- [Scenario-Schematic100x100](https://github.com/xlandscape/Scenario-Schematic100x100) (Version: 2.3)

## Models
Models use one or multiple components to run simulations in a *scenario* (see above). Examples are [the effects of pyrethroids to aquatic invertebrates in a river catchment](https://pubs.acs.org/doi/10.1021/acs.est.3c02716), or [the fate of plant protection products in off-field soils](https://academic.oup.com/ieam/article/20/1/263/7725049).

The following models are currently available:

- [xAquaticRisk](https://github.com/xlandscape/xAquaticRisk) (Version: 2.85)  
- [xNTTP](https://github.com/xlandscape/xNTTP) (Version: 0.10)  
- [xOffFieldSoilRisk](https://github.com/xlandscape/xOffFieldSoilRisk) (Version: 1.4.6)  
- [xCropProtectionDemo](https://github.com/xlandscape/xCropProtectionDemo) (Version: 1.2)  
 Description: A xLandscape model for demonstrating the CropProtection component



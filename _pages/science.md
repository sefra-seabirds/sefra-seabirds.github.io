---
title: "SEFRA"
permalink: /science/
layout: single
---

<style>body {text-align: justify}</style>

The Spatially Explicit Fisheries Risk Assessment (SEFRA[^1]) framework has been developed and utilised in New Zealand and is now standard procedure for estimating the risk to seabirds from commercial fishing[^2][^3][^4]. The approach is designed to accommodate multiple species and fisheries simultaneously, constructing risk profiles as a function of spatial and temporal overlap. Application has been primarily within the New Zealand Exclusive Economic Zone (EEZ), but, since seabirds can migrate widely across the southern hemisphere, a comprehensive assessment of the fisheries risk needs to account for all the fishing effort that may be encountered as they move through international waters. This, as well as the need to inform management outside of the New Zealand EEZ, has motivated application of the method in this wider context[^5][^6][^7][^8][^9][^10].

The SEFRA approach is a quasi-spatial model where temporal and spatial overlap of the seabird distribution and fishing effort are used as a covariate with which to predict the captures. Parameterisation of the capture rate per unit of overlap occurs via a fit to fisheries observer capture data, and total captures are then calculated by multiplication of the total overlap (including the unobserved component) with this estimated rate (referred to as the catchability). Deaths are calculated from the predicted captures using a mortality multiplier that accounts for the probability of dead capture and cryptic mortality. Following estimation of the total deaths, the SEFRA approach attempts to quantify the risk using a limit reference point referred to as the Population Sustainability Threshold (PST[^1]):

\begin{equation}
\text{Risk ratio}=  \frac{\text{Deaths}}{\text{PST}}
\end{equation}

\begin{equation}
\mathrm{PST} =  \frac{1}{2} \cdot \phi \cdot r_{\mathrm{max}} \cdot N
\end{equation}

where $\phi$ is an adjustment used by management to ensure that deaths equal to the PST correspond to a defined population stabilisation or recovery objective; $r_{\mathrm{max}}$ is the theoretical unconstrained maximum population growth rate (i.e., under optimal conditions and in the absence of density dependent constraints); and, $N$ is the population size for that species.

If $N$ is the total population size, then it is possible to underestimate the impact of fishing if only a subset of the population is exposed. For the New Zealand context, it was recommended by an independent review that modelling should focus on the adult population only, as there was observed to be a dearth of juvenile captures in domestic fisheries[^11]. This decision can also be influenced by data availability, such as the inadequacy of biological and distributional information from immature birds, as well as ambiguity in capture data caused by difficulty in distinguishing maturity stage. For recent domestic applications of SEFRA, $N$ therefore refered to the adult population size[^4] and the most recent southern hemisphere assessment applied the same assumption[^10].

The PST estimates the total amount of additional death a population can sustain (above natural mortality) whilst still meeting the population recovery goal. However, deaths estimated by SEFRA are typically only a subset of the total anthropogenic mortality. This is most obvious when only a subset of the total fishing effort is being included, but there may also be non-fishery related deaths that are not accounted for. When the deaths estimated by SEFRA correspond to an unknown proportion of total deaths, then comparing those deaths to the PST may be misleading, and not represent a true indication of the prospects for long-term population viability. However, it is still the case that $r_{\mathrm{max}}$ and $N$ are important for determining the relative risk between species: for a given number of deaths a large or productive population can be considered at lower risk, all else being equal. For instances in which the risk ratio cannot be properly calculated, we instead use a relative mortality measure:
\begin{equation}
\text{Relative mortality}=  \frac{\text{Deaths}}{r_{\mathrm{max}} \cdot N} \label{eqn:relmort}
\end{equation}
where $r_{\mathrm{max}} \cdot N$ is equal to the theoretical maximum growth rate in numbers per year. The relative mortality approach still provides the same relative ranking as that achieved using the PST reference point, because the $\phi$ term is typically assumed to be the same for all species during comparative assessments. 

To estimate deaths there first needs to be an estimate of captures. To do this a capture rate per unit of overlap, per fishery group and species group, is required. This capture rate is known as the ``catchability'' and the catchability coefficient $q$ is estimated using the observed portion of effort data. It is then applied to the total effort to obtain the predicted total seabird captures. The catchability is usually estimated for a species group rather than a species, as this allows for the capture records of more abundant species to supplement more sparse data from rare and threatened species. The quality of capture records in terms of the ability of observers to determine species identification through either direct observation or dedicated necropsy programmes is an important component of how models are structured. When species identification is reliable, species-specific terms can be utilised to allows the catchability to deviate from the fixed fishery and species group effects in a manner dependent on the information content of the data.

Calculating the overlap between fishery group and species group is a critical step in the SEFRA methodology. Considerations for the desired resolution of final results for relevant management purposes and privacy of participating fisheries must be taken into account when defining fisheries groups. Species group should be defined with consideration of the likely accuracy of identifications of seabird captures at differing taxonomic resolutions, as well as the likely accuracy of distribution maps given available tracking data.

In the New Zealand domestic context fishery groups have been defined by method, vessel characteristics and seabird mitigation requirements[^2]. For application in tuna Regional Fisheries Management Organizations (tRFMOs), the fleet of individual members for a management organisation can each be treated as one fishery fleet, except where there is evidence of clear operational or vessel characteristic differences between a proportion of the fleet. In the context of the Commission for the Conservation of Southern Bluefin Tuna (CCSBT) such a distinction could be made for the Japanese joint-venture operation under New Zealand's flag. This is due to differences in vessel size and operational characteristics between the joint-venture operation and the domestic the New Zealand surface longline fleet, as well as the strict management and surveillance requirements under the joint venture arrangement. For those fisheries groups with no available observed capture data, a proxy value of $q$ can be obtained from a fleet with similar operational characteristics, such as operating area, vessel size, mitigation requirements and gear configuration. 

Similarly to fishery group, species group is determined according to their feeding behaviour and aggression, and willingness to travel large distances to a fishing vessel. A catchability coefficient is shared across species within a species group, by assuming that their vulnerability to fishing is determined by these shared behavioural characteristics. Recent assessment of risk at the southern hemisphere scale have been targeted to cover the 27 Agreement for the Conservation of Albatross and Petrels (ACAP) species[^12] (with additional distinction between Antipodean albatross *Diomedea antipodensis antipodensis* and Gibson’s albatross *Diomedea antipodensis gibsonii*, and Northen Buller’s albatross *Thalassarche bulleri platei* and Southern Buller’s albatross *Thalassarche bulleri bulleri*) that inhabit this region[^10]. These species were assigned into six species groups: wandering albatross, royal albatross, small albatross, sooty albatross, large petrel, and medium petrel. The list of species assessed, along with their species group, is given in this [Table](/objective/). 

Finally, to estimate deaths a multiplier of mortality resulting from fisheries interactions and the proportion of interactions that are unobservable must be applied to captures. The estimated mortality resulting from interactions is the mortality rate of live captures post release. The most conservative approach is to apply a 99% mortality rate to live captures (effectively treating all captures as dead) in the absence of studies to determine the true proportion.  The proportion of interactions that are unobservable is accounted for by applying a cryptic multiplier. When PST is used or when multiple fishing methods are assessed in the same SEFRA this value is important in assessing the probability of achieving population stabilisation or a recovery objective, or the relative impact of different methods respectively. In the context of assessing relative mortality between fisheries groups of a single fishing method this parameter is less important as it is applied as a single scalar. Dedicated research has been undertaken to inform these scalars as they directly relate to fisheries being assessed[^13], but it remains a considerable source of uncertainty.

## Suitability of SEFRA for ecological risk assessment by tRFMOs
The third report of the ''Kobe Process'' (Kobe III) identified the importance of continued efforts to harmonise tRFMO bycatch and fishing data, and to develop common data confidentiality rules with surrounding protocols on the types of data that can be shared and how it can be used[^14]. Although there is currently no formal central repository for data sharing among all tRFMOs, steps made with the WCPFC-IATTC Data Exchange show that there is both a need and a mechanism for this to occur. In addition to the recommendations of Kobe III, the substantial overlap in membership between the various tRFMOs, all requiring routine reporting, incentivises the adoption of standardised reporting as a way of simplifying this requirement for members and cooperating non-members. By ensuring that the requirements of SEFRA fit within the data standards agreed to by the various tRFMOs, and given the common need for ecosystem management reiterated as part of Kobe III, the approach outlined in this document is a method that can be readily applied.

The SEFRA approach for exploring spatial and temporal risk to bycatch species has been applied successfully in the New Zealand context to marine mammals, seabirds and sharks[^15][^16][^17][^18] and when coupled with resulting management actions can be used to manage fisheries risk[^19]. As such, the SEFRA approach has been adapted to meet the needs of CCSBT members in exploring risk to seabirds but can be variously adapted to undertake work with other by-catch species.

## Context for the application of SEFRA by the CCSBT
The issue of incidental bycatch of seabirds in southern bluefin tuna (SBT) fisheries was well recognised even at the time of establishment of the Commission for the Conservation of Southern Bluefin Tuna (CCSBT) in 1994. An initial draft of recommendations on reducing this bycatch was developed in 2006 at the 6th meeting of the CCSBT Ecologically Related Species Working Group (ERSWG). In 2008 CCSBT agreed on the need to assess impact on species considered under the ERSWG and in 2018 a resolution to align CCSBT’s ecologically related species (ERS) measures with those of other tuna Regional Fisheries Management Organisations (tRFMOs) was adopted at the 25th Annual Meeting.

At the 13th meeting of the CCSBT ERSWG in 2019, an initial assessment of global seabird bycatch among all tRFMOs through the Areas Beyond National Jurisdiction (ABNJ) Tuna Project was concluded[^20]. Alongside this assessment, commitments to develop a ERSWG workplan led to the CCSBT Multi-year Seabird Strategy, which was adopted at the 26th Annual Meeting of CCSBT.

A range of actions to be undertaken under each specific objective of the Multi-year Seabird Strategy was developed at the 14th meeting of ERSWG in 2021 and adopted by the 29th Annual meeting of CCSBT, which included an action to ''update SEFRA seabird risk assessment,'' with New Zealand and Japan taking a leading role, and was successfully concluded in 2024[^21]. The current project is a continuation of this work. As well as meeting the objectives of the CCSBT ERSWG, it is hoped that it will provide a foundation for work across tRFMOs by developing methods suitable for assessing the incidental bycatch of seabird in their respective fisheries.

-----------------------------------

[^1]: Sharp, B.R. (2019). Spatially Explicit Fisheries Risk Assessment: A framework for quantifying and managing incidental commercial fisheries impacts on non-target species. Chapter 3, pp. 18–55, in Ministry for Primary Industries (2019). Aquatic Environment and Biodiversity Annual Review 2018. Compiled by the Fisheries Science Team, Ministry for Primary Industries, Wellington New Zealand. 704 p.

[^2]: Richard, Y.; Abraham, E.R.; Berkenbusch, K. (2017). Assessment of the risk of commercial fisheries to New Zealand seabirds, 2006–07 to 2014–15. New Zealand Aquatic Environment and Biodiversity Report No. 191.

[^3]: Richard, Y.; Abraham, E.R.; Berkenbusch, K. (2020). Assessment of the risk of commercial fisheries to New Zealand seabirds, 2006–07 to 2016–17. New Zealand Aquatic Environment and Biodiversity Report No. 237.

[^4]: Edwards, C.T.T.; Peatman, T.; Goad, D.; Webber, D.N. (2023). Update to the risk assessment for New Zealand seabirds. New Zealand Aquatic Environment and Biodiversity Report No. 314.

[^5]: Susan M. Waugh, S.M.; Filippi, D.P.; Sharp, B.R.; Weimerskirch, H. (2012) Ecological Risk Assessment for seabird interactions in surface longline fisheries managed under the Convention for the Conservation of Southern Bluefin Tuna. CCSBT-ERS/1203/09 (Rev.1)

[^6]: Abraham, E.; Richard, Y.; Walker, N.; Gibson, W.; Daisuke, O.; Tsuji, S.; Kerwath, S.; Winker, H.; Parsa, M.; Small, C.; Waugh, S. (2017). Assessment of the risk of surface longline fisheries in the Southern Hemisphere to albatrosses and petrels, for 2016. Report to the CCSBT ERSWG (CCSBT-ERS/1905/17)

[^7]: Abraham, E.R.; Richard, Y.; Walker, N.; Roux, M.J. (2017). Assessment of the risk of commercial surface longline fisheries in the southern hemisphere to ACAP seabird species. Report to the CCSBT ERSWG (CCSBT-ERS/1905/BGD 03)

[^8]: Abraham, E.R.; Richard, Y.; Walker, N.; Roux, M.J. (2017). Assessment of the risk of Southern Hemisphere surface longline fisheries to ACAP species. Report to the Western and Central Pacific Fisheries Commission Scientific Committee (WCPFC-SC13-2017/EB IP-13)

[^9]: Ochi, D.; Abraham, E.; Inoue, Y.; Oshima, K.;Walker, N.; Richard, Y.; Tsuji, S. (2018). Preliminary assessment of the risk of albatrosses by longline fisheries. Report to the WCPFC Scientific Committee 3rd Regular Session. (WCPFC-SC14-2018/ EB-WP-09 Rev1)

[^10]: Edwards, C.T.T.; Peatman, T.; Roberts, J.O.; Devine, J.A.; Hoyle, S.D. (2023). Updated fisheries risk assessment framework for seabirds in the Southern Hemisphere. New Zealand Aquatic Environment and Biodiversity Report No. 321.

[^11]: Lonergan, M.E.; Phillips, R.A.; Thomson, R.B.; Zhou, S. (2017). Independent review of New Zealand’s Spatially Explicit Fisheries Risk Assessment approach - 2017. New Zealand Fisheries Science Review 2017/2 36 p.

[^12]: ACAP (2015). Albatross and petrel species to which the agreement applies. https://acap.aq/ acap-species/307-acap-species-list/file. [Accessed on 4-Aug-2024].

[^13]: Baker, G.; Candy, S.; Parker, G. (2021). Improving estimates of cryptic mortality for use in seabird risk assessments: loss of seabirds from longline hooks. New Zealand Aquatic Environment and Biodiversity Report No. 268. 7 p.

[^14]: ICCAT (2011). Chair’s report of the joint third meeting of the tuna regional fisheries management organisations (kobe iii). , International Commission for the Conservation of Atlantic Tunas.

[^15]: Large, K.; Roberts, J.; Francis, M.; Webber, D. (2019). Spatial assessment of fisheries risk for New Zealand sea lions at the Auckland Islands. New Zealand Aquatic Environment and Biodiversity Report No. 224. 85 p.

[^16]: MacKenzie, D.I.; Meyer, S.; Pavanato, H.; Fletcher, D. (2023). Updated spatially explicit fisheries risk assessment for New Zealand marine mammal populations. New Zealand Aquatic Environment and Biodiversity Report No. 290. 218 p.

[^17]: Roberts, J.; Webber, D.; Roe, W.; Edwards, C.T.T.; Doonan, I. (2019). Spatial risk assessment of threats to hector’s and maui dolphins (*Cephalorhynchus hectori*). New Zealand Aquatic Environment and Biodiversity Report No. 214. 168 p.

[^18]: Edwards, C.T.T. (2023). Development of spatial fisheries risk assessment methods for sharks and turtles in New Zealand waters. New Zealand Aquatic Environment and Biodiversity Report No. 319. 94 p.

[^19]: MPI and DOC (2021). Hector’s and maui dolphin threat management plan 2020. Final report to New Zealand Department of Conservation, New Zealand Department of Conservation Te Papa Atawhai and Fisheries New Zealand Tini a Tangaroa.

[^20]: BLI (2019) Report of the Final Global Seabird Bycatch Assessment Workshop Seabird Bycatch Component for Output 3.2.1 of the Sustainable Management of Tuna Fisheries and Biodiversity Conservation in the ABNJ 25 February – 1 March 2019 Skukuza Conference center, Kruger National Park, South Africa.

[^21]: CCSBT (2024). Report of The Fifteenth Meeting of the Ecologically Related Species Working Group, Commission for the Conservation of Southern Bluefin Tuna. 4 – 7 June 2024 Tokyo, Japan. 110 p.





















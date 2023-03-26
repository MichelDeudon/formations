---
title: Super hydrophobie
date: '2023-01-29'
type: book
weight: 30
tags:
  - Superhydrophobie
---

From Young's angle to the Fakir effect

<!--more-->

## Introduction

Many examples of superhydrophobia exist in nature. This property allows lotus and ginkgo biloba leaves to stay dry and clean in order to convert CO2 more efficiently into oxygen through photosynthesis. This same property allows most birds to take off directly from the water, with a few exceptions such as the cormorant, whose hydrophilic feathers soak up water (the reason why we see it perched, drying off after diving).

The measurement of the Young's angle defined as the angle formed between a surface and a drop of water placed on it, makes it possible to characterize hydrophilic surfaces from hydrophobic surfaces. A drop of water placed on a hydrophilic surface, such as wood, has a tendency to conform to the shape of the surface, whereas on a superhydrophobic surface, it forms a pearl. This beading property has inspired the design of waterproof garments like K-ways.

In the following, we are interested in club club spores, a fern-like plant that appeared 470 million years ago. Its microscopic spores are superhydrophobic and would have allowed the plant to populate the Earth by crossing the oceans.

## Overview of Lycopodium spores

{{< figure src="super-hydrophoby/img4.png" caption="Diagram of experimental setup for determining spore size." numbered="true">}}

The diffraction of light makes it possible to determine the size of the spores. The measurement of the apparent diameter of the Airy disk {{< math >}}$\theta${{< /math >}} illustrated in Figure 1 makes it possible to go back to their diameter D by the relation {{< math >} }$\theta = 1.22 \frac{\lambda}{D}${{< /math >}}. Numerically, we find {{< math >}}$D\approx 20 \mu m${{< /math >}}.

Club moss spores are covered by two envelopes, one
internal called endospore, the other external called exospore. The exospore is made of sporopollenin, a natural polymer whose exact composition is still unknown because sporopollenin is very inert. However, studies have shown that the structure of sporopollenin is close to that of {{< math >}}$\beta${{< /math >}} carotene, and obtained from ferulic acid and p-coumaric acid [1]. The presence of long carbon chains would explain their hydrophobicity.

{{< figure src="super-hydrophoby/img2.png" caption="Representation of ferulic acid (left) and p-coumaric acid (right)." numbered="true">}}

The observation of spores under an optical microscope (x100, x400, x600) suggests that their surface is not smooth.
Distant irregularities
a few {{< math >}}$\mu m${{< /math >}} make it rough and superhydrophobic. This is the Fakir effect: a drop of water does not crush under the effect of gravity but leaves pockets of air under it, like a fakir resting on nails. This occurs when the distance between the irregularities is less than the capillary length of water {{< math >}}$L_c = \sqrt{\frac{\gamma}{\rho g}} \approx 3${{ < /math >}} mm.

{{< figure src="super-hydrophoby/img3.jpg" caption="Lycopodium spores, seen under a microscope." numbered="true">}}

### Drawing an energy diagram

{{< figure src="super-hydrophoby/img1.jpg" caption="Illustration of the coalescence phenomenon" numbered="true">}}

Two drops coated with lycopodium spores do not coalesce, a property that can be used to transport a liquid in a fluid [2]. On the other hand, if a drop has enough energy, coalescence can occur. In [3], the authors determine the critical impact velocity for a drop of variable radius R to pass through a spore layer. We will study here the energy barrier represented by spores for the coalescence of water droplets. We consider water drops of constant volume {{< math >}}$\approx \mu m^3 ${{< /math >}}. We denote by {{< math >}}$R${{< /math >}} their radius.

{{< figure src="super-hydrophoby/img5.png" caption="Schematic of the experimental device to study the energy required for a drop of water to cross a surface covered with spores." numbered="true">}}

### Assembly and protocol

The schematic of the experimental setup is shown in Figure 3. {{< math >}}$S${{< /math >}} defines the area of ​​the beaker, {{< math >}}$m${{< / math >}} the deposited spore mass and {{< math >}}$\sigma = \frac{m}{S}${{< /math >}}
the surface density of spores, assumed to be uniform on the scale of the beaker. With {{< math >}}$\sigma${{< /math >}} fixed, I varied {{< math >}}$h${{< /math >}}, the height from which the water drop is released without initial velocity, the spore interface being marked with {{< math >}}$h=0${{< /math >}}. As a first approximation, the impact velocity is {{< math >}}$v=\sqrt{2gh}${{< /math >}}. The experimental result is binary, either the drop crosses the surface, or it does not cross it.

### Statistic study

At {{< math >}}$\sigma${{< /math >}} and h set, I successively released between 5 and 10 drops. The result is a fraction comprised
between 0 (no dropped drops passed through the spores) and 1 (all dropped drops passed through).
So, given {{< math >}}$\sigma${{< /math >}}, iterating the above for different values ​​of h, I define two heights {{< math >}}$h_{min }${{< /math >}} and {{< math >}}$h_{max}${{< /math >}}.

If {{< math >}} $h < h_{min}$ {{< /math >}} the drop never crosses and if {{< math >}} $h > h_{max}$ {{< / math >}} the drop still goes through: the energy input is sufficient. The interval {{< math >}}$[h_{min}-h_{max}]${{< /math >}} corresponds to the measurement uncertainties.

After more than 800 drops dropped, I got an energy diagram where {{< math >}}$\sigma${{< /math >}} is plotted on the abscissa, {{< math >}}$h_{min }${{< /math >}} and {{< math >}}$h_{max}${{< /math >}} ordered. Three areas can be distinguished. A prime where {{< math >}}$h${{< /math >}} is proportional to {{< math >}}$\sqrt{\sigma}${{< /math >}}, then a linear and finally quadratic evolution. We also notice that there is a critical areal density {{< math >}}$\sigma_c${{< /math >}}. If {{< math >}}$\sigma< \sigma_c${{< /math >}} a drop of water crosses the layer of spores, whatever its height of fall.

{{< figure src="super-hydrophobia/img6.png">}}

### Modeling local spore depletion

#### Statement of principle

When the deformation of the interface is maximum (state marked by * and depending on the height of fall h),
if the apparent areal density {{< math >}}$\sigma^*${{< /math >}} is less than {{< math >}}$\sigma_c${{< /math >}}, the drop crosses.
Otherwise the drop does not cross. The limiting case {{< math >}}$\sigma^*=\sigma_c${{< /math >}} corresponds to the boundary between the two regimes. To determine {{< math >}}$\sigma^*${{< /math >}} given the parameters {{< math >}}$h${{< /math >}} and {{< math >}}$\sigma${{< /math >}}, I went to the d'Alembert de Jussieu institute to film the deformation. Arnaud Antkowiak, professor at UPMC and researcher in fluid mechanics, welcomed me and allowed me to make videos with a fast camera (more than 1000 images per second).

#### Linear domain modeling

{{< figure src="super-hydrophoby/img7.png" caption="Example in the linear domain of the energy diagram." numbered="true">}}

The photo sequences show that in this area, it
there are no spore projections. The conservation of matter results in
{{< math >}}$$
    S^* \sigma^*=S\sigma
$${{< /math >}}
As a first approximation, the deforming spore surface is directly below the drop. The variation of the area is therefore given by
{{< math >}}$$
    \Delta S = S^* - S \approx \Pi R^2 (\frac{\sigma}{\sigma^*}-1)
$${{< /math >}}
Furthermore, the conservation of energy results in
{{< math >}}$$
    \rho (\frac{4}{3} \pi R^3) gh= \gamma \Delta S
$${{< /math >}}
where the term on the left corresponds to the potential energy of the dropped drop of water, and the term on the right corresponds to the variation in surface energy due to its deformation.
The energy diagram equation is obtained by replacing {{< math >}}$\sigma^*${{< /math >}} by {{< math >}}$\sigma_c${{< /math > }} in equations (2) and (3). We do indeed obtain a linear relation between {{< math >}}$h${{< /math >}} and {{< math >}}$\sigma${{< /math >}}, valid for {{ < math >}}$\sigma \geq \sigma_c${{< /math >}}
{{< math >}}$$
    h \approx \frac{4}{3} \frac{\gamma}{\rho Rg} (\frac{\sigma}{\sigma_c}-1)
$${{< /math >}}
{{< math >}}$h${{< /math >}} is proportional to {{< math >}}$\gamma${{< /math >}} and inversely proportional to the mass of the drop d water, that seems consistent.

### Conclusion

For a drop of water to actually cross Lycopodium spores of surface density {{< math >}}$\sigma${{< /math >}}, a sufficient supply of kinetic energy is needed to allow
a consequent local depletion of spores. The transfer and exchange of energy are decisive in the nature of the response.

### Reference

[1] S. Barrier. [Physical and chemical properties of sporopollenin exine particles](https://core.ac.uk/download/pdf/9841868.pdf). PhD Thesis. University of Hull. 2008.

[2] P. Aussillous. [Les gouttes enrobées](https://theses.hal.science/tel-00003630). PhD Thesis. Université Paris VI. 2002.

[3] E. Lorenceau, C. Planche, A. L. Biance et al. [Coalescence of armored interface under impact](https://aip.scitation.org/doi/abs/10.1063/1.4801320). 2013.

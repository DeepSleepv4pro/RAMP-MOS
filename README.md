# RAMP-MOS
Abstract—Independent motion encoding and full-image
mask decoding add computational overhead to moving
object segmentation. Full-image processing incurs computation beyond the foreground region. We propose RAMP-MOS, a region-adaptive motion-prompted segmentation
framework that combines feature reuse with local mask
decoding. A shared visual feature pyramid provides appearance representations and coarse motion estimates.
Motion candidates are aggregated into a motion region
of interest, whose extent is adjusted according to the
reliability of the motion responses. The relative region
scale and internal motion density jointly define an effective
foreground scale indicator for selecting feature levels or
their combinations. Local residual motion features are
combined with a soft prior propagated from previous
probability maps to form a dense prompt that guides mask
decoding within the selected region. The model is evaluated
on seven public benchmarks, has 61.88M parameters, and
achieves a region similarity of 89.3% on DAVIS17 Motion
under binary foreground evaluation. On the DAVIS 2016
validation set, local decoding reduces the average floating point operation count by 17.1% relative to full-image
decoding at the same input resolution and parameter
count, with a decrease of 0.4 percentage points in region
similarity. On MoCA, retaining the historical-prior-related
branches improves the bounding-box localization success
rate by 14.7 percentage points at an intersection-over-union
threshold of 0.5 compared with removing these branches.

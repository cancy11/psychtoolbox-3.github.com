# [kPsychUse32BPCFloatAsap](kPsychUse32BPCFloatAsap)
##### >[Psychtoolbox](Psychtoolbox)>[PsychGLImageProcessing](PsychGLImageProcessing)

rval = kPsychUse32BPCFloatAsap  
  
Return a flag that you can pass to the 'imagingmode' parameter of  
[Screen](Screen)('OpenWindow') in order to request support for internal  
framebuffers that store color information with 32 bits per color  
component in floating point format if this is supported by the graphics  
hardware without any restrictions.  
  
If you hardware is able to support all its functions (especially  
framebuffer blending) without restrictions then all framebuffers will be  
configured to 32 bpc precision. This should be the case on ATI Radeon HD  
2000 and [NVidia](NVidia) Geforce 8000 hardware. On older hardware, which is limited  
in its functionality when using 32 bpc framebuffers (e.g., the very  
useful framebuffer blending doesn't work), PTB will allocate a lower  
precision 16 bpc float framebuffer as initial framebuffer for user code  
drawing. All further processing of the content of that 16 bpc framebuffer  
will be carried out using 32 bpc precision framebuffers.  
  
This function is a workaround for old hardware. If you intend to do lots  
of serious work with HDR imagery or high contrast precision displays, do  
yourself a favor and buy a current generation graphics card.  
  




<div class="code_header" style="text-align:right;">
  <span style="float:left;">Path&nbsp;&nbsp;</span> <span class="counter">Retrieve <a href=
  "https://raw.github.com/Psychtoolbox-3/Psychtoolbox-3/beta/Psychtoolbox/PsychGLImageProcessing/kPsychUse32BPCFloatAsap.m">current version from GitHub</a> | View <a href=
  "https://github.com/Psychtoolbox-3/Psychtoolbox-3/commits/beta/Psychtoolbox/PsychGLImageProcessing/kPsychUse32BPCFloatAsap.m">changelog</a></span>
</div>
<div class="code">
  <code>Psychtoolbox/PsychGLImageProcessing/kPsychUse32BPCFloatAsap.m</code>
</div>


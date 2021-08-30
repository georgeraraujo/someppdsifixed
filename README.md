# someppdsifixed
Some PPDs (PostScript Printer Description files) I fixed for the following printer models:

- Xerox Phaser 6600DN (en)
- Xerox Phaser 6600N (en)
- Xerox WorkCentre 6605DN (en)
- Xerox WorkCentre 6605N (en) 

Before:

```
$ cupstestppd *.ppd
xr6600dn.ppd: FAIL
      **FAIL**  Unable to open PPD file - OpenGroup without a CloseGroup first on line 353.
                REF: Pages 45-46, section 5.2.
        WARN    Non-Windows PPD files should use lines ending with only LF, not CR LF.

xr6605dn.ppd: FAIL
      **FAIL**  Unable to open PPD file - OpenGroup without a CloseGroup first on line 353.
                REF: Pages 45-46, section 5.2.
        WARN    Non-Windows PPD files should use lines ending with only LF, not CR LF.

xrx6600n.ppd: FAIL
      **FAIL**  Unable to open PPD file - OpenGroup without a CloseGroup first on line 336.
                REF: Pages 45-46, section 5.2.
        WARN    Non-Windows PPD files should use lines ending with only LF, not CR LF.

xrx6605n.ppd: FAIL
      **FAIL**  Unable to open PPD file - OpenGroup without a CloseGroup first on line 336.
                REF: Pages 45-46, section 5.2.
        WARN    Non-Windows PPD files should use lines ending with only LF, not CR LF.
```

After:

```
xr6600dn.ppd: PASS
        WARN    DefaultGuaranteedMaxSeparations has no corresponding options.

xr6605dn.ppd: PASS
        WARN    DefaultGuaranteedMaxSeparations has no corresponding options.

xrx6600n.ppd: PASS
        WARN    DefaultGuaranteedMaxSeparations has no corresponding options.

xrx6605n.ppd: PASS
        WARN    DefaultGuaranteedMaxSeparations has no corresponding options.
```

Only tested the Xerox WorkCentre 6605DN, which is what I have - worked OK.

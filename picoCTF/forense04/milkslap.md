# MilkSlap

# Description
🥛
# Solution

-  Once I  am in the web page righth click on the image , copy link and then I download the image using wget once I tried to use ```zsteg``` but I found out an error.

``` bash
wget http://mercury.picoctf.net:48380/concat_v.png
zsteg -a concat_v.png 
/var/lib/gems/3.0.0/gems/zpng-0.4.5/lib/zpng/scan_line.rb:369:in `prev_scanline_byte': stack level too deep (SystemStackError)
	from /var/lib/gems/3.0.0/gems/zpng-0.4.5/lib/zpng/scan_line.rb:319:in `block in decoded_bytes'
	from /var/lib/gems/3.0.0/gems/zpng-0.4.5/lib/zpng/scan_line.rb:318:in `upto'
	from /var/lib/gems/3.0.0/gems/zpng-0.4.5/lib/zpng/scan_line.rb:318:in `decoded_bytes'
	from /var/lib/gems/3.0.0/gems/zpng-0.4.5/lib/zpng/scan_line/mixins.rb:17:in `prev_scanline_byte'
	from /var/lib/gems/3.0.0/gems/zpng-0.4.5/lib/zpng/scan_line.rb:377:in `prev_scanline_byte'
	from /var/lib/gems/3.0.0/gems/zpng-0.4.5/lib/zpng/scan_line.rb:319:in `block in decoded_bytes'
	from /var/lib/gems/3.0.0/gems/zpng-0.4.5/lib/zpng/scan_line.rb:318:in `upto'
	from /var/lib/gems/3.0.0/gems/zpng-0.4.5/lib/zpng/scan_line.rb:318:in `decoded_bytes'
	 ... 10225 levels...
	from /var/lib/gems/3.0.0/gems/zsteg-0.2.13/lib/zsteg.rb:26:in `run'
	from /var/lib/gems/3.0.0/gems/zsteg-0.2.13/bin/zsteg:8:in `<top (required)>'
	from /usr/local/bin/zsteg:25:in `load'
	from /usr/local/bin/zsteg:25:in `<main>'
	
```

- I solve the error by increasing the stack of ruby and finally I get the flag

```bash

```

-  final step

```bash

```
# Additional notes

Any additional note
# References
- [Reference links](youtube.com)

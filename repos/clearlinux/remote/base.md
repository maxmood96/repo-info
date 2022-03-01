## `clearlinux:base`

```console
$ docker pull clearlinux@sha256:1fd7a9edc1ed428b7868901bd5438b1b4fabdd3292bd19e41828feb1b4298c11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clearlinux:base` - linux; amd64

```console
$ docker pull clearlinux@sha256:1891cd1def3aa4bbebd23a444ab3e40de6b98304d79130271c782fc5d21e631c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.4 MB (87441323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31c2ec945aa0a7a2287fdfae0c70ae1d0625ba40c7da6e6719bdb4ee1fde1247`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 09 Mar 2021 00:22:54 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Tue, 01 Mar 2022 02:05:31 GMT
ADD file:18434ec815fd361ff1613ffc33b7979595a4cc5e3fbbfe475274e1f4d63b2f8c in / 
# Tue, 01 Mar 2022 02:05:32 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     grep root /usr/share/defaults/etc/shadow > /etc/shadow
# Tue, 01 Mar 2022 02:05:32 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:f3136dff1762ef5a847e13a025b27bc2e54c322aeb67b40dbcd7aa0972344a06`  
		Last Modified: Tue, 01 Mar 2022 02:05:55 GMT  
		Size: 87.4 MB (87441105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4bb01963c22a8ed3b0d714f71962cf4d81728b4a57a63215424b79c66aa67be`  
		Last Modified: Tue, 01 Mar 2022 02:05:43 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

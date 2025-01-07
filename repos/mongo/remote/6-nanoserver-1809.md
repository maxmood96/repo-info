## `mongo:6-nanoserver-1809`

```console
$ docker pull mongo@sha256:18f642091dd9d5ac1636a966643bf75be7251ee0ad565374a2519e10da3bbf57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6659; amd64

### `mongo:6-nanoserver-1809` - windows version 10.0.17763.6659; amd64

```console
$ docker pull mongo@sha256:e0c164ef7bb2db687b993c4df545465bf19233c33d11560fe54b2bb40cff59f9
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **681.3 MB (681334465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32c5518a7c7adb11661fc9c1e0e3b28985995dada2e5db3e1f1ade2ccfe166b9`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Thu, 05 Dec 2024 04:54:21 GMT
RUN Apply image 10.0.17763.6659
# Wed, 11 Dec 2024 21:49:14 GMT
SHELL [cmd /S /C]
# Wed, 11 Dec 2024 21:49:15 GMT
USER ContainerAdministrator
# Wed, 11 Dec 2024 21:49:17 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Wed, 11 Dec 2024 21:49:18 GMT
USER ContainerUser
# Wed, 11 Dec 2024 21:49:19 GMT
COPY multi:a15cb83b582227fb63ddd0661404eaa1493105c6dda1936a8da7d2c4ac1b40ba in C:\Windows\System32\ 
# Wed, 11 Dec 2024 21:49:20 GMT
ENV MONGO_VERSION=6.0.19
# Wed, 11 Dec 2024 21:49:39 GMT
COPY dir:f97029ff7a52e12f6b8e5522b58ebccd35083615a35a3126b84db5898f526c7b in C:\mongodb 
# Wed, 11 Dec 2024 21:49:53 GMT
RUN mongod --version
# Wed, 11 Dec 2024 21:49:54 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 11 Dec 2024 21:49:54 GMT
EXPOSE 27017
# Wed, 11 Dec 2024 21:49:55 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:fc1cdf36537340b1875b5d6573a58a268fc20b63dc54a780f9070e51cf9eb9ca`  
		Last Modified: Tue, 10 Dec 2024 21:03:34 GMT  
		Size: 155.2 MB (155231618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7304242e1dc3729d0d71968ffd40cb7b23cf9363c006763250c18d42800b0df`  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7efff41b185eebdaf780e145450ce63ae3c7c13153d2460a57d3ff6f13585eb`  
		Last Modified: Wed, 11 Dec 2024 21:50:08 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da4a90eec4111214bd44f221357e17b9fa59a4a89cc8cc085357145ae58fa9d5`  
		Size: 71.1 KB (71067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be253a80de58b4c908fc8670307e6fe0ea8786f08748f7f03838535ac138aa31`  
		Last Modified: Wed, 11 Dec 2024 21:50:02 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:392461be2aa0205c81dd3ccd2244a23938473886597d99400e7639b961ba02d0`  
		Last Modified: Wed, 11 Dec 2024 21:50:01 GMT  
		Size: 275.1 KB (275139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:818bb5cbc56f7d75921ac8581a0182c928bce6758e9744822cec29749374a25a`  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a52c75f7692fffae999d307aea775f51120d14759800b60d8555eeb9d2caee9`  
		Last Modified: Wed, 11 Dec 2024 21:50:39 GMT  
		Size: 525.7 MB (525677034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4deb51c891911e45e2a3305f6a13928e92babf2fd7587905b4283c1abc80c6bf`  
		Last Modified: Wed, 11 Dec 2024 21:49:58 GMT  
		Size: 72.3 KB (72270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f620c9e7de1ee48a616ea590c61876bf6c22f0ccfc65d1a552720b122a321974`  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14a4776b3059053564e858331de39ef326ddcb49fad6e5f037c768ba6601f184`  
		Last Modified: Wed, 11 Dec 2024 21:49:58 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc4104054453eea1b6a2d8ab169fe09e5e1602e94364e0b97b8d57e260fc9875`  
		Last Modified: Wed, 11 Dec 2024 21:50:01 GMT  
		Size: 1.0 KB (1049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

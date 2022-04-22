## `sapmachine:lts`

```console
$ docker pull sapmachine@sha256:c5fd3687e68b521238e3fdf8a58cba3c0c4c5b25861a27da33a811852ddf6581
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `sapmachine:lts` - linux; amd64

```console
$ docker pull sapmachine@sha256:eb7659ab20223f149f5f7df29ca8d570b326804aca40ebc3cf0e6f57139930eb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.5 MB (234531401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7290c4fedecdd8d519986ae0b14d2c10a813c7d9afd05e31e5c3b0a7670e0a65`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 21 Apr 2022 23:00:07 GMT
ADD file:064c61cc9ceed678689d2eaf3b3e61ec3bf5baf9288e5a7febcbab28c6adbfb6 in / 
# Thu, 21 Apr 2022 23:00:07 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 03:56:18 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:58:00 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && wget -q -O - https://dist.sapmachine.io/debian/sapmachine.old.key | gpg --batch --import     && gpg --batch --export --armor 'DA4C 00C1 BDB1 3763 8608 4E20 C7EB 4578 740A EEA2' > /etc/apt/trusted.gpg.d/sapmachine.old.gpg.asc     && wget -q -O - https://dist.sapmachine.io/debian/sapmachine.key | gpg --batch --import     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/amd64/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.2     && rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:58:01 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Fri, 22 Apr 2022 03:58:01 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:8e5c1b329fe39c318c0d49821b339fb94a215c5dc0a2898c8030b5a4d091bcba`  
		Last Modified: Sun, 17 Apr 2022 03:03:46 GMT  
		Size: 28.6 MB (28565998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bff95dd8c1098ae71dc81b04acfd2d3daf018131b8193361347566dac0fe084d`  
		Last Modified: Fri, 22 Apr 2022 03:58:18 GMT  
		Size: 8.3 MB (8317757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e7540cfea05a9f68d05978eb8265628437464b58e87584361960143dc99b633`  
		Last Modified: Fri, 22 Apr 2022 03:59:22 GMT  
		Size: 197.6 MB (197647646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

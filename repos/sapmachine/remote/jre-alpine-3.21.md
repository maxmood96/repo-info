## `sapmachine:jre-alpine-3.21`

```console
$ docker pull sapmachine@sha256:b4dda41d570702393a073401c3f224ae888d912909c254ec5d316ce61aa38046
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:jre-alpine-3.21` - linux; amd64

```console
$ docker pull sapmachine@sha256:ea21976c8dd26744ccdeb853279ec543b7b111cb45aa41a2b70e9105f9b50f32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.5 MB (61489893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e3362aa9efde19e7b2f150f287db3ff648bfdd02b1c6a0731b4baa636a52f6c`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Wed, 21 Jan 2026 20:03:01 GMT
RUN wget -qO /etc/apk/keys/sapmachine-apk.rsa.pub https://dist.sapmachine.io/alpine/sapmachine-apk.rsa.pub &&     echo "4444e47cabf35695f9406692848de191d3b7cbd47dcdc1ffb62f4f70aea06e89 /etc/apk/keys/sapmachine-apk.rsa.pub" | sha256sum -c - &&     echo "https://dist.sapmachine.io/alpine" >> /etc/apk/repositories &&     apk add sapmachine-25-jre=25.0.2-r0 # buildkit
# Wed, 21 Jan 2026 20:03:01 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-sapmachine-jre
# Wed, 21 Jan 2026 20:03:01 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:f637881d1138581d892d9eb942c56e0ccc7758fe3bdc0f1e6cd66059fdfd8185`  
		Last Modified: Sun, 07 Dec 2025 13:55:07 GMT  
		Size: 3.6 MB (3642569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5595453c86ad283eb51a5939bb2762c39867b76a060455538ae37b37a3922717`  
		Last Modified: Wed, 21 Jan 2026 20:03:13 GMT  
		Size: 57.8 MB (57847324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-alpine-3.21` - unknown; unknown

```console
$ docker pull sapmachine@sha256:e7e4d2095cab1da7dbc600796b3307c0293c891e6c05cc2ead10914dea9485f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **440.3 KB (440346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf80703a1b5968ba3af257057b537c9049a868051843e57e88f56aa357911c99`

```dockerfile
```

-	Layers:
	-	`sha256:69211853195e6dcdb3fca2ec944cc42d6e197517c5a6ee9f537d4959a665c57e`  
		Last Modified: Wed, 21 Jan 2026 22:16:48 GMT  
		Size: 432.7 KB (432733 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4a3f741bef8fcf10bc5fd249088b10e156e5278249903b943f7d4f6c08dabb5`  
		Last Modified: Wed, 21 Jan 2026 22:16:54 GMT  
		Size: 7.6 KB (7613 bytes)  
		MIME: application/vnd.in-toto+json

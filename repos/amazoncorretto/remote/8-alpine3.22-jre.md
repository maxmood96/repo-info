## `amazoncorretto:8-alpine3.22-jre`

```console
$ docker pull amazoncorretto@sha256:f3940110db59695ac465cfc612a5c886c8b3d1fad7144a6ccca2ec135a769cc1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-alpine3.22-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:fab01340d3662bbc80616e8cedfed624439a0624ad6dfa2cfa41d2ab40aa5fb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45546276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c87731a527fba5c088baf3e708a6d286afadb96b21ae540ce7d7246618ee151`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 21 Jan 2026 18:58:32 GMT
ARG version=8.482.08.1
# Wed, 21 Jan 2026 18:58:32 GMT
# ARGS: version=8.482.08.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Wed, 21 Jan 2026 18:58:32 GMT
ENV LANG=C.UTF-8
# Wed, 21 Jan 2026 18:58:32 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:21 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fce3f7b4a16346b192b2f8f6a6ed6413ab04383fb60865d70dcc34f4d113f2b4`  
		Last Modified: Wed, 21 Jan 2026 18:58:50 GMT  
		Size: 41.7 MB (41743824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.22-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:9929ba1d79a423ecb9ed350dd9b5dd5c450bde6ab95739cf877da837f6c31b31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.1 KB (197145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:293fd29fab5d60a5b6112f2abbbb53f197131ec6835511166b83d91307a2fb4a`

```dockerfile
```

-	Layers:
	-	`sha256:32a1c6d8c8ab3a8999b72feca43cc9520bf17743ed090fe2b0a63fdac8073333`  
		Last Modified: Wed, 21 Jan 2026 18:58:41 GMT  
		Size: 188.5 KB (188490 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55b54a34d975c3db6dd5bbb8fbdb4a37b742cadbc6ced58e7ae35af5ba40d948`  
		Last Modified: Wed, 21 Jan 2026 19:56:21 GMT  
		Size: 8.7 KB (8655 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-alpine3.22-jre` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:d63ab47bb0a857c3aad2e4689c1b6910aa60b28374e802fe0b51f4f32b5f9993
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.6 MB (45596250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:825dad3aee85fc5d1399aeb2284d57adbe00cd7388bc6f29d836bb38b5dfe965`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 21 Jan 2026 18:58:36 GMT
ARG version=8.482.08.1
# Wed, 21 Jan 2026 18:58:36 GMT
# ARGS: version=8.482.08.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Wed, 21 Jan 2026 18:58:36 GMT
ENV LANG=C.UTF-8
# Wed, 21 Jan 2026 18:58:36 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:11 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ccc627f49a1826bb4139cd35304d733c7fc6625f1175cdb145e2f7e30e1595e`  
		Last Modified: Wed, 21 Jan 2026 20:04:15 GMT  
		Size: 41.5 MB (41458181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.22-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:491e1ab953b14d58cc7794001d82f5fcba23affd4b7d81b815452a985de7d782
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.3 KB (197334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:693df936bf23004d3df5c19971bfeae37a481f442aada8f57837230ce83e79f4`

```dockerfile
```

-	Layers:
	-	`sha256:cbf1ce4445978621799c3bcc20e94d645c0cd247d31c38ec4d070f085fdacb9b`  
		Last Modified: Wed, 21 Jan 2026 19:56:44 GMT  
		Size: 188.6 KB (188598 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a99292e4907c58ef27bfbbfefeaa673f2dc9e2ae65855c1f58cc79040422fa6a`  
		Last Modified: Wed, 21 Jan 2026 18:58:45 GMT  
		Size: 8.7 KB (8736 bytes)  
		MIME: application/vnd.in-toto+json

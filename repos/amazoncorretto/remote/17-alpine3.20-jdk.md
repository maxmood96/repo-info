## `amazoncorretto:17-alpine3.20-jdk`

```console
$ docker pull amazoncorretto@sha256:84165faafd11b331f8fc655548d51744e3bb93f2d95028617898ec47eb538739
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-alpine3.20-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:88af8fa732ba58ead848e72fd23d1df947bc06f459b1522f70e155907c928d57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.2 MB (152202806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e4f36e8866f3473a231af357510ddf185a625e01b95edcdd4dc927b890217d2`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:26 GMT
ADD alpine-minirootfs-3.20.10-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:26 GMT
CMD ["/bin/sh"]
# Wed, 22 Apr 2026 21:34:13 GMT
ARG version=17.0.19.10.1
# Wed, 22 Apr 2026 21:34:13 GMT
# ARGS: version=17.0.19.10.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip # buildkit
# Wed, 22 Apr 2026 21:34:13 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 21:34:13 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 22 Apr 2026 21:34:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:25f1d6b1951ac8eb3740558fe94cb83d377bdadf95fd9f98b50d2e1b96130471`  
		Last Modified: Thu, 16 Apr 2026 23:53:31 GMT  
		Size: 3.6 MB (3630321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a880e403bea770b094be73db5eff74bca3ac0bb0726ce4bdc5ac6534335f0af`  
		Last Modified: Wed, 22 Apr 2026 21:34:30 GMT  
		Size: 148.6 MB (148572485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-alpine3.20-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:5177c457f042f7a57056249e0b26383ae08ba4b3c647e541aa7d0ef2c3469d65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **590.7 KB (590679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6aad1272135e121e5a268d32dd82b08d9eafdd60bcc03127ef423ac38067ecd5`

```dockerfile
```

-	Layers:
	-	`sha256:0340c56fd4b59e7e49907bafeb83142e18fae18fda223b57ef05c43c0b0e998e`  
		Last Modified: Wed, 22 Apr 2026 21:34:27 GMT  
		Size: 581.3 KB (581300 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b987b6f0e616a0ef4556e16a5344f03864de5e47c87c9d31e0a526b7cadd94a1`  
		Last Modified: Wed, 22 Apr 2026 21:34:26 GMT  
		Size: 9.4 KB (9379 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-alpine3.20-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:5feccca4e23f2aa49770fd3d42b7a2792a866d2ade48b8d8ec0c8195965132ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.0 MB (151033647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd429a92427dfbfe00e2685d717c4246a6cd0d80f14c76935155dfb5423b61c9`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:24 GMT
ADD alpine-minirootfs-3.20.10-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:24 GMT
CMD ["/bin/sh"]
# Wed, 22 Apr 2026 21:34:06 GMT
ARG version=17.0.19.10.1
# Wed, 22 Apr 2026 21:34:06 GMT
# ARGS: version=17.0.19.10.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip # buildkit
# Wed, 22 Apr 2026 21:34:06 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 21:34:06 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 22 Apr 2026 21:34:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:3f26bc2dec0b515f1c2818f6e13a8f1da1f88179a008445d4e587233386bff78`  
		Last Modified: Thu, 16 Apr 2026 23:53:29 GMT  
		Size: 4.1 MB (4092319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4058ca4eea785c20dedb9e35f64168b9076a61644339a156f702a202d1aa8a1`  
		Last Modified: Wed, 22 Apr 2026 21:34:25 GMT  
		Size: 146.9 MB (146941328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-alpine3.20-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:07cdb412f997647934e11509dc8639328558b03e282dd615075f23778eb39855
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **590.2 KB (590202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaca01f681ec5a3b08cd71303047a30fb74f5f5017d95c66be4a6e2df264da20`

```dockerfile
```

-	Layers:
	-	`sha256:1ffd18edfe72b46ce6ed1f75b2f84eb232ee1a2bc676fada13a598d245c6fd0d`  
		Last Modified: Wed, 22 Apr 2026 21:34:22 GMT  
		Size: 580.7 KB (580719 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dbfa020a873f5179873ccdefb83de2a02100a4282b9090d9e65d9e5d861d9f37`  
		Last Modified: Wed, 22 Apr 2026 21:34:22 GMT  
		Size: 9.5 KB (9483 bytes)  
		MIME: application/vnd.in-toto+json

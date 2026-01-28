## `amazoncorretto:25-alpine-full`

```console
$ docker pull amazoncorretto@sha256:f38bd37ff06d1257e10a60b23ef257f8fc6a57254f7c6505370fee22f000cccd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:25-alpine-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:c20b42e7f7ddca31cec1f7c72f69f771e941253d1812b3f065c9d3d0a8a2aea1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.6 MB (184621110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bc3ccf703effdf9f798547fbc1d95dfb3b4db0896c32557eda228e31b14ae74`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:52:59 GMT
ARG version=25.0.2.10.1
# Wed, 28 Jan 2026 02:52:59 GMT
# ARGS: version=25.0.2.10.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-25=$version-r0 &&     rm -rf /usr/lib/jvm/java-25-amazon-corretto/lib/src.zip # buildkit
# Wed, 28 Jan 2026 02:52:59 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:52:59 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 28 Jan 2026 02:52:59 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce024e0c1fc281f3f61f3cf3a1e72dcd0c8f1a01d7b36ccd799f9d0d0de6c041`  
		Last Modified: Wed, 28 Jan 2026 02:53:20 GMT  
		Size: 180.8 MB (180759289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-alpine-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:83f8b889c6eac116004788a41ae274df9760cca74dd3d990709c75cc85c5399a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **602.8 KB (602814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:459def8437806487585d0f721d3eadc0c8f5d24d0f0f7b0db8df26548d24babc`

```dockerfile
```

-	Layers:
	-	`sha256:f51030d32bec29592c094e88edd4e7d6b718ec2bc68137242922f62a7fb69733`  
		Last Modified: Wed, 28 Jan 2026 02:53:16 GMT  
		Size: 592.1 KB (592136 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c8becfde8dddef8d841f4959ba8657cc9747f2eec30f49a57d31200109f31bb`  
		Last Modified: Wed, 28 Jan 2026 02:53:16 GMT  
		Size: 10.7 KB (10678 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:25-alpine-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:cc5b7d3e6bb705ddc3dba4488234805502bf108bfb025702ff3ca13f33135139
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.6 MB (182607999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b469899e525a802426be7e62ce8924433ea174c0d2bb78d11d2a4d86317add9d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Wed, 21 Jan 2026 19:02:07 GMT
ARG version=25.0.2.10.1
# Wed, 21 Jan 2026 19:02:07 GMT
# ARGS: version=25.0.2.10.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-25=$version-r0 &&     rm -rf /usr/lib/jvm/java-25-amazon-corretto/lib/src.zip # buildkit
# Wed, 21 Jan 2026 19:02:07 GMT
ENV LANG=C.UTF-8
# Wed, 21 Jan 2026 19:02:07 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 21 Jan 2026 19:02:07 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:35 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be75faa7526db811aa2909c9e3b63266e0f0527bbd5eb98b347274fcfdeb975a`  
		Last Modified: Wed, 21 Jan 2026 19:02:30 GMT  
		Size: 178.4 MB (178412260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-alpine-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:36c18f939388c3e021ba9faa27b2d80a44dec66e6d4372e150396bd8ebc85426
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **601.8 KB (601780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af893bafa57fb4622825d916e0b9b188fcfd7f95d31a2128dc44b397cffb6e4e`

```dockerfile
```

-	Layers:
	-	`sha256:814edccdc5e4923331312e3e95e4416d4c963dd0c667d0a41a6665f8b81f8304`  
		Last Modified: Wed, 21 Jan 2026 19:02:24 GMT  
		Size: 591.0 KB (590950 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30392ce3ff3aafd2c8103cc67332068cea44f7de68d28e2337cfbd76c62226c5`  
		Last Modified: Wed, 21 Jan 2026 19:02:24 GMT  
		Size: 10.8 KB (10830 bytes)  
		MIME: application/vnd.in-toto+json

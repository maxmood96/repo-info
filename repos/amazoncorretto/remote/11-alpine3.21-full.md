## `amazoncorretto:11-alpine3.21-full`

```console
$ docker pull amazoncorretto@sha256:bfa6903a17b31292ad000bd4aa84f259f5637c6707cd7c988556380b42483028
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-alpine3.21-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:c3d59040ca56863d03683c9a92226d9a9bf1e729a10e636ccfad6913f8fa7ecb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.2 MB (147226633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ccdf9444c18d4f3fc37757c827acc24c5c61cabb6a62cd1b1b07f22f1e4b05e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:43 GMT
ADD alpine-minirootfs-3.21.6-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:43 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:45:21 GMT
ARG version=11.0.30.7.1
# Wed, 28 Jan 2026 02:45:21 GMT
# ARGS: version=11.0.30.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0 &&     rm -rf /usr/lib/jvm/java-11-amazon-corretto/lib/src.zip # buildkit
# Wed, 28 Jan 2026 02:45:21 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:45:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 28 Jan 2026 02:45:21 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:bc1da058f299723f8258c5a82dd007d1dd72e275087b726d5e1be5ef6198f286`  
		Last Modified: Wed, 28 Jan 2026 01:18:49 GMT  
		Size: 3.6 MB (3643742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c2732d781a6d3bb0cf7d06b3c76b875a07c2c8afeff3763810b8cb85626a7fa`  
		Last Modified: Wed, 28 Jan 2026 02:45:38 GMT  
		Size: 143.6 MB (143582891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-alpine3.21-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:d8eb30346be111328295dfe7b0bdd541b778569d23434244363a2744545fbd03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **602.7 KB (602733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1d91d594bcd3d66e3775823ebad257389e5c9b726071f50fe707d598f8a5993`

```dockerfile
```

-	Layers:
	-	`sha256:87dcbe73c5381ea14633ff632ba592dd10bc905e75aed23003f62ea5f75871cd`  
		Last Modified: Wed, 28 Jan 2026 02:45:35 GMT  
		Size: 593.4 KB (593359 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f37222c39a657466205ed466d93db6e7c277d569612901918699b97787cc8fb`  
		Last Modified: Wed, 28 Jan 2026 02:45:35 GMT  
		Size: 9.4 KB (9374 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-alpine3.21-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:3118af31af61d6b785b97b95d59ab993682036940bbb97170e0c20ecb6ac6ed7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.8 MB (145840417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:289099a30d9cb9f1fe893bd3b7b05615324e31f2eb16b9e7cb457c4e3d52aaac`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Wed, 21 Jan 2026 19:00:09 GMT
ARG version=11.0.30.7.1
# Wed, 21 Jan 2026 19:00:09 GMT
# ARGS: version=11.0.30.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0 &&     rm -rf /usr/lib/jvm/java-11-amazon-corretto/lib/src.zip # buildkit
# Wed, 21 Jan 2026 19:00:09 GMT
ENV LANG=C.UTF-8
# Wed, 21 Jan 2026 19:00:09 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 21 Jan 2026 19:00:09 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:c2fe130f4aabc917e559e7eed7d37b0e21ba13b44520101696887ca892e8c63f`  
		Last Modified: Wed, 08 Oct 2025 12:04:23 GMT  
		Size: 4.0 MB (3992353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a04a593c5f3bac99587bb3c97f2d47b7ed042402fb3e2a103f22220c2df492d`  
		Last Modified: Wed, 21 Jan 2026 19:00:26 GMT  
		Size: 141.8 MB (141848064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-alpine3.21-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:b9d2487adca8a3160dddba2fe68cbf7ba80644259516f69802e9d615f64c9db2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **602.9 KB (602893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d248a7a6a4a7cf397438763a2350249ec88be35e6fceb070134aa6c06bc1c906`

```dockerfile
```

-	Layers:
	-	`sha256:6ce4eb74aef68ea3abec03d8952de3d48744c628901a9dd605182868500b830c`  
		Last Modified: Wed, 21 Jan 2026 19:00:24 GMT  
		Size: 593.4 KB (593415 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24964eddeb615fb540dec2ce552445df3fa8958306acc5641ad501d3db6dbcbe`  
		Last Modified: Wed, 21 Jan 2026 19:00:23 GMT  
		Size: 9.5 KB (9478 bytes)  
		MIME: application/vnd.in-toto+json

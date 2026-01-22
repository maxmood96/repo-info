## `amazoncorretto:11-alpine3.21`

```console
$ docker pull amazoncorretto@sha256:2976a12a93488b01e925414256719aa4ac973717e3fe23294f99cbec3328e3f0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-alpine3.21` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:aeab86b664f65a6416ce016339f9ba799258addb271b0ce8b778b4e45eab6b44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.2 MB (147225561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13e5c26856a034fd54b7f0ffeea5cc3777b7cba9ec7ee50b79532924d15b6eca`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Wed, 21 Jan 2026 18:59:59 GMT
ARG version=11.0.30.7.1
# Wed, 21 Jan 2026 18:59:59 GMT
# ARGS: version=11.0.30.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0 &&     rm -rf /usr/lib/jvm/java-11-amazon-corretto/lib/src.zip # buildkit
# Wed, 21 Jan 2026 18:59:59 GMT
ENV LANG=C.UTF-8
# Wed, 21 Jan 2026 18:59:59 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 21 Jan 2026 18:59:59 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:f637881d1138581d892d9eb942c56e0ccc7758fe3bdc0f1e6cd66059fdfd8185`  
		Last Modified: Sun, 07 Dec 2025 13:55:07 GMT  
		Size: 3.6 MB (3642569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbd4d4585f595d417b50542a4e1f2e89ab91822dd6afdcc67e05d648b5d79d0a`  
		Last Modified: Wed, 21 Jan 2026 20:09:51 GMT  
		Size: 143.6 MB (143582992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-alpine3.21` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:dfbdc1a53e513046f9d3715e3875b486d854c3dd90717bfd40b60163da8ddd84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **602.7 KB (602732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dd4cf661dbc16036546341b4353b75f90348986315855213a21f67e4961bbc9`

```dockerfile
```

-	Layers:
	-	`sha256:0da861d7a33559d8ae2cb664683710e678f27a7253baabac285925957aa5d20f`  
		Last Modified: Wed, 21 Jan 2026 19:48:32 GMT  
		Size: 593.4 KB (593359 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d31820fb5d8c5452905fe88a5a6abf2e69f86e279605c3ab9f84af825bb6c522`  
		Last Modified: Wed, 21 Jan 2026 19:00:12 GMT  
		Size: 9.4 KB (9373 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-alpine3.21` - linux; arm64 variant v8

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
		Last Modified: Sun, 07 Dec 2025 17:54:48 GMT  
		Size: 4.0 MB (3992353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a04a593c5f3bac99587bb3c97f2d47b7ed042402fb3e2a103f22220c2df492d`  
		Last Modified: Wed, 21 Jan 2026 19:00:26 GMT  
		Size: 141.8 MB (141848064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-alpine3.21` - unknown; unknown

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
		Last Modified: Wed, 21 Jan 2026 19:48:34 GMT  
		Size: 593.4 KB (593415 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24964eddeb615fb540dec2ce552445df3fa8958306acc5641ad501d3db6dbcbe`  
		Last Modified: Wed, 21 Jan 2026 19:00:23 GMT  
		Size: 9.5 KB (9478 bytes)  
		MIME: application/vnd.in-toto+json

## `amazoncorretto:8u482-alpine3.22`

```console
$ docker pull amazoncorretto@sha256:53cf8db51b20fba0a37011813894ccc0c76a951fb42dff073a2712201bb3b7f7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8u482-alpine3.22` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:feb90c3858bcef23c5d11124fa574f33c4f0324595fcadde74d1f0b235f94f95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.6 MB (104583003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a9997e85dc1c5c73b2419a963b60136d3cdd5bdf443211f76f9b265f7318e64`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:22:17 GMT
ARG version=8.482.08.1
# Fri, 17 Apr 2026 00:22:17 GMT
# ARGS: version=8.482.08.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Fri, 17 Apr 2026 00:22:17 GMT
ENV LANG=C.UTF-8
# Fri, 17 Apr 2026 00:22:17 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 17 Apr 2026 00:22:17 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5c91606da9fdc7f60ba6f9ba261b1571a141d9bdecf994d39a79b602c13f771`  
		Last Modified: Fri, 17 Apr 2026 00:22:32 GMT  
		Size: 100.8 MB (100774814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u482-alpine3.22` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:37e276c08d62b014701eb11c8b486cf9f0d953a813e63fe827ef46bec155aa69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.0 KB (257029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2113e17e072ff901418447b1c4a267ebc89143b970b1f9d70c8aea3706caa525`

```dockerfile
```

-	Layers:
	-	`sha256:26b837c6002fe213109edc563186f7f462c3bfec646fd30e48865fe131633bfd`  
		Last Modified: Fri, 17 Apr 2026 00:22:29 GMT  
		Size: 247.7 KB (247674 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:83b7cdbc758f2e6dd1139c7f398b4dc9b4a5cee2770efad5ca597002b94e6740`  
		Last Modified: Fri, 17 Apr 2026 00:22:29 GMT  
		Size: 9.4 KB (9355 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8u482-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:b955d82e8df075990f9fc1132ef15cacc40a47b6ec095bab7db0e992ec13f74e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.7 MB (104703178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bd96b12376d0da0d1b5addec545dadcd7b442e5b258ae69fa4ffd297de563ba`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:00 GMT
ADD alpine-minirootfs-3.22.4-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:00 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:24:17 GMT
ARG version=8.482.08.1
# Fri, 17 Apr 2026 00:24:17 GMT
# ARGS: version=8.482.08.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Fri, 17 Apr 2026 00:24:17 GMT
ENV LANG=C.UTF-8
# Fri, 17 Apr 2026 00:24:17 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 17 Apr 2026 00:24:17 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:58e777220c395c319866c5d73ea32a5ea574bbd12f4eb289b392f584d0cd953e`  
		Last Modified: Thu, 16 Apr 2026 23:53:05 GMT  
		Size: 4.1 MB (4141894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dda2ffb4f4685028a0355a1798d9b2976d2be0b6ac6afb01833edfbb66e034e9`  
		Last Modified: Fri, 17 Apr 2026 00:24:36 GMT  
		Size: 100.6 MB (100561284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u482-alpine3.22` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:6300e799e4b78936cfa5e9d72480c37de6f4c5a2e5eae3cd129cce0266e0364a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.3 KB (257265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4140951c27eeb0f0721bbc574dfb8b8fcbdc980d5cb146a7b9435048e6d5f6e2`

```dockerfile
```

-	Layers:
	-	`sha256:ce41d423f83b059781c1ee06d4b66fcca787c66b668e3570b6a84d52f11563ff`  
		Last Modified: Fri, 17 Apr 2026 00:24:29 GMT  
		Size: 247.8 KB (247806 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41f8328fd2558969f0224bcdd80a04aa66c7d68cedab1729a6c2e999e91fd29c`  
		Last Modified: Fri, 17 Apr 2026 00:24:29 GMT  
		Size: 9.5 KB (9459 bytes)  
		MIME: application/vnd.in-toto+json

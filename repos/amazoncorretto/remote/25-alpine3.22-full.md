## `amazoncorretto:25-alpine3.22-full`

```console
$ docker pull amazoncorretto@sha256:e3818f93bee840c1593492ba5335ceb214ffe4a37a8275e49d23aab6f66b9f6a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:25-alpine3.22-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:05241de317d97075ef119aa844d5cfdac464faeb3a47a53e4196046ad9e2fc9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.5 MB (184527864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:013ebc5da418432afbf6e0f1cc84cffeee90eae5217d035476531c7a657f6ce3`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 05 Nov 2025 01:07:20 GMT
ARG version=25.0.1.9.1
# Wed, 05 Nov 2025 01:07:20 GMT
# ARGS: version=25.0.1.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-25=$version-r0 &&     rm -rf /usr/lib/jvm/java-25-amazon-corretto/lib/src.zip # buildkit
# Wed, 05 Nov 2025 01:07:20 GMT
ENV LANG=C.UTF-8
# Wed, 05 Nov 2025 01:07:20 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 05 Nov 2025 01:07:20 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39efdfa875cf11df5af65d4582d8a8c511a684ff9b183b51bad538fe768d8495`  
		Last Modified: Wed, 05 Nov 2025 04:50:28 GMT  
		Size: 180.7 MB (180725412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-alpine3.22-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:75c8b205c4c4b97d3b58f07ca9215def2c39aac8d0863bd344d7acfb9c9638b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **604.1 KB (604118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06844a18a78d42b29f2e2bad145994f32d22b4b81837bc8343a7eaa63ad1785c`

```dockerfile
```

-	Layers:
	-	`sha256:27079c04b0a09c9cd7c8e4076a18d9384f0af334785a334d8015536da209fe69`  
		Last Modified: Wed, 05 Nov 2025 04:49:41 GMT  
		Size: 593.4 KB (593441 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64db07a7e63f8a38b1855a460c68a17c48a5261bb8dbc9d9fc8cac2dfd3d28c8`  
		Last Modified: Wed, 05 Nov 2025 04:49:42 GMT  
		Size: 10.7 KB (10677 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:25-alpine3.22-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:97012dc6b91f7cdfe350518ad6fc9d958005dc51b605f41313a1d5624264b7a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.5 MB (182509705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c0311fff7ede045dbc300a8663c82c45551ac40d6598ef136df77a8b7a6b604`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 04 Nov 2025 23:16:08 GMT
ARG version=25.0.1.9.1
# Tue, 04 Nov 2025 23:16:08 GMT
# ARGS: version=25.0.1.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-25=$version-r0 &&     rm -rf /usr/lib/jvm/java-25-amazon-corretto/lib/src.zip # buildkit
# Tue, 04 Nov 2025 23:16:08 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 23:16:08 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 04 Nov 2025 23:16:08 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6c3d1078166ba6eb65daea030105157330eb50995e58c176b24e5eb82842fb4`  
		Last Modified: Tue, 04 Nov 2025 23:27:31 GMT  
		Size: 178.4 MB (178371636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-alpine3.22-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:4f14430e35a42f7ab27493b3c053017e63d2da0f2f79a5a792f9d2a21f4e2c8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **603.7 KB (603734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2678f9c1db66106173206e1c56cb2ff211b377d651da7e3660b2f4a49cb15c0e`

```dockerfile
```

-	Layers:
	-	`sha256:3e82b505ff1b0ded503f6c5693dd4fe39832d9f51f677b8be5dcea084afbb030`  
		Last Modified: Wed, 05 Nov 2025 00:28:45 GMT  
		Size: 592.9 KB (592905 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d65138cd816fe5bc1e5472fd4f5ea7d8d1ff2afccafd955cd91808cd66cdd43e`  
		Last Modified: Wed, 05 Nov 2025 00:28:45 GMT  
		Size: 10.8 KB (10829 bytes)  
		MIME: application/vnd.in-toto+json

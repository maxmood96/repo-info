## `amazoncorretto:23-alpine3.17-full`

```console
$ docker pull amazoncorretto@sha256:05fcdb6c59793bc71ba2f38e4130def3823cb3bfe054676d1a54ab30bb5703a2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:23-alpine3.17-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:6faa5d085b8be463f91a80a3ba76003255343439c8e79993ec3e11720c687619
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.0 MB (170031568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a864ae68766957c84fdee7717aceada89f64f8e824b57d51bd3fa873bf8da61b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:24 GMT
ADD file:8bf458f5fbed9f27c897506538c02fb5810b70aba850bb883d2120985fa15bac in / 
# Fri, 06 Sep 2024 22:20:25 GMT
CMD ["/bin/sh"]
# Thu, 19 Sep 2024 23:46:25 GMT
ARG version=23.0.0.37.1
# Thu, 19 Sep 2024 23:46:25 GMT
# ARGS: version=23.0.0.37.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-23=$version-r0 &&     rm -rf /usr/lib/jvm/java-23-amazon-corretto/lib/src.zip # buildkit
# Thu, 19 Sep 2024 23:46:25 GMT
ENV LANG=C.UTF-8
# Thu, 19 Sep 2024 23:46:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Thu, 19 Sep 2024 23:46:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:a0f4cbe03b6df9e61ce02b3c41bbc05481842858bd48d9687614abe719303b47`  
		Last Modified: Fri, 06 Sep 2024 22:21:07 GMT  
		Size: 3.4 MB (3392194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f21ad81bd42c5f79d41013e607f233e213f5df4566930b84e4ff0972ff66907`  
		Last Modified: Fri, 20 Sep 2024 23:56:05 GMT  
		Size: 166.6 MB (166639374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:23-alpine3.17-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:d710d16361d22b6c4c5a07834716af3145c0f67eac90750d5fbe00606acb0d1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 KB (11551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b588c65c22cee657a65501e8df74c46b4e2c6b5bcfac0c18858c39f478fae9c1`

```dockerfile
```

-	Layers:
	-	`sha256:6ffc2339485212e6704ce524bacc033006d1c4b3d1bf080dfbac58a97178947f`  
		Last Modified: Fri, 20 Sep 2024 23:56:02 GMT  
		Size: 2.4 KB (2381 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f2f90daf6e9e277c41b52fc2bf17162424c83386969d020300985cbfac4798fe`  
		Last Modified: Fri, 20 Sep 2024 23:56:02 GMT  
		Size: 9.2 KB (9170 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:23-alpine3.17-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:b1e1b93e94c36368f9c7c1ad7f6a7c9912808d9cc31e44628840d8734345c85a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.6 MB (167585967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06f59af466f022c671f8d3ded992207cb4f40cc8ae31eceab78c981f333ab084`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:24 GMT
ADD file:e3f989df31d7e2d820078058c5d0ed7d98695c5b86bd172276270ebb59d75ee6 in / 
# Fri, 06 Sep 2024 22:44:24 GMT
CMD ["/bin/sh"]
# Thu, 19 Sep 2024 23:46:25 GMT
ARG version=23.0.0.37.1
# Thu, 19 Sep 2024 23:46:25 GMT
# ARGS: version=23.0.0.37.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-23=$version-r0 &&     rm -rf /usr/lib/jvm/java-23-amazon-corretto/lib/src.zip # buildkit
# Thu, 19 Sep 2024 23:46:25 GMT
ENV LANG=C.UTF-8
# Thu, 19 Sep 2024 23:46:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Thu, 19 Sep 2024 23:46:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:4a3d188841b4b0359cda0d73dc5f89f8bc569f3bcb178cfd0507b4ead0db7bf4`  
		Last Modified: Fri, 06 Sep 2024 22:45:06 GMT  
		Size: 3.3 MB (3275072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51f11c87e93862257dae5500b1ea4553456ddbb2cc9f8339ad5e2565c3e0d422`  
		Last Modified: Fri, 20 Sep 2024 23:58:40 GMT  
		Size: 164.3 MB (164310895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:23-alpine3.17-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:7d89627d79120eada0b9de0d45088e3f555ec30dbda13929802cc2e7de97e667
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **390.2 KB (390242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f96746346c2bf48595604be6a0832bb6cdecf3f7ca6a4f300ccfe2499952024`

```dockerfile
```

-	Layers:
	-	`sha256:dbd989f9cd058be4c50e429048dd6bcfc2cdd292aaf623b16d4985fc5ec0331b`  
		Last Modified: Fri, 20 Sep 2024 23:58:36 GMT  
		Size: 380.8 KB (380772 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5bfcb5fd14a9bed6b2856d777d857a0a41507bd6968743a946aec0a010777e6d`  
		Last Modified: Fri, 20 Sep 2024 23:58:36 GMT  
		Size: 9.5 KB (9470 bytes)  
		MIME: application/vnd.in-toto+json

## `amazoncorretto:17-alpine3.19-full`

```console
$ docker pull amazoncorretto@sha256:1eef0810b35c2135773fdef9136eb803456a14aaa9e9f564033d0cb55d12ffeb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-alpine3.19-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:7ab9dd3170ae090b17cebe288f2a707e406b8b4792132db7dab2f30e12976749
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.4 MB (149437053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f130ca3cb52e319328246a029cc2541a5792d5d9ed13402d63718478a450cbaf`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
ADD file:c644b15c170e2ca46176a566910d40a21dce66518ed8fdfd34ebcf0e9dc90c55 in / 
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/sh"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=17.0.12.7.1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=17.0.12.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 16 Jul 2024 22:56:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:46b060cc26202cf98e28414d790b5cabd67094bba50315a1ae2e9daf913fca4f`  
		Last Modified: Mon, 22 Jul 2024 22:27:25 GMT  
		Size: 3.4 MB (3419040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdad945e55a69e381ba8bc3a0972a33ac83c2c5acc8569b6368eaca7448eb088`  
		Last Modified: Mon, 22 Jul 2024 23:04:48 GMT  
		Size: 146.0 MB (146018013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-alpine3.19-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:08bbba5498b40eef85c3d1801bd3262a247c721da3bf45d0f78cabb93fc95cf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **389.9 KB (389935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b522794bcc3b8eb441338a890047f311384b283371df56ceaa3f4678575cb629`

```dockerfile
```

-	Layers:
	-	`sha256:6e7ba5cf08af4fbb7a15eeff3eb53b7e9d590ec2d2d3033e0f825eda8aaaacb9`  
		Last Modified: Mon, 22 Jul 2024 23:04:46 GMT  
		Size: 380.8 KB (380763 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d75ff49673ff2301a4cf9ce4349f358b623f5a14ec9178e1dd5c9d3b033c79c5`  
		Last Modified: Mon, 22 Jul 2024 23:04:46 GMT  
		Size: 9.2 KB (9172 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-alpine3.19-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:b5723e477abe7d6243853d7a9b9e800691ff9c743b42adeaf20a789224cc15b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.7 MB (147707956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93c9f82b0e8a92f40219145a967261b83ce485d4aaf15cfb511a7e3e1c1c5810`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 20 Jun 2024 17:40:38 GMT
ADD file:f5632bd5469a9b26f7ff1739bb0b5dd166613259104f7bf76d587a8a428debcc in / 
# Thu, 20 Jun 2024 17:40:38 GMT
CMD ["/bin/sh"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=17.0.12.7.1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=17.0.12.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 16 Jul 2024 22:56:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:d4f2d2bd5ed999e04bfbfb910f14154b488ad32abf053954bff805f47fc3ad1e`  
		Last Modified: Thu, 20 Jun 2024 17:41:12 GMT  
		Size: 3.4 MB (3357202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b78f93404a7937c552ee4b89eaf805ea5e47d0425d072569573bd426fd17911e`  
		Last Modified: Thu, 18 Jul 2024 01:17:31 GMT  
		Size: 144.4 MB (144350754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-alpine3.19-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:c8809d5b88c3e4d24289cb23d16dfcb2999b8fedc9b4403d50af4a604bd5b33a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **389.7 KB (389653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe04ad1df87956ceec0bd72322dcf7e7ad03a3f0b4c363bca3cc6e5ffb5a12f1`

```dockerfile
```

-	Layers:
	-	`sha256:915885e241d846a2cc4cfac72ea30eb9ef88b101949ec704d98b91235cbfbbea`  
		Last Modified: Thu, 18 Jul 2024 01:17:27 GMT  
		Size: 380.2 KB (380181 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1029adacc1b98b3b0880b27d4acaf4c0f4f5f3d70b0ffb40c3f6730ef5d9143d`  
		Last Modified: Thu, 18 Jul 2024 01:17:27 GMT  
		Size: 9.5 KB (9472 bytes)  
		MIME: application/vnd.in-toto+json

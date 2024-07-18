## `amazoncorretto:8u422-alpine3.18`

```console
$ docker pull amazoncorretto@sha256:1739af40803c46471f8e85581bb294350babc20a01778dab7385d340c87ee2f0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8u422-alpine3.18` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:d1e643c90db3347f5bd75960a9bc1793cc7957989941497f469c4f6bbf26bc3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.5 MB (103537709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b63c9b1440cf38bd6bb34d32c224a122d88b01deab4b8520259615ce2e51f731`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 20 Jun 2024 20:17:10 GMT
ADD file:aa183dc07d0f6a47c02f7f1388fa0ce4639ad328111172149be7c7c65d634ded in / 
# Thu, 20 Jun 2024 20:17:10 GMT
CMD ["/bin/sh"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=8.422.05.1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=8.422.05.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 16 Jul 2024 22:56:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:73baa7ef167e70f1c0233fe09e741780d780ea16e78b3c1b6f4216e2afbbd03e`  
		Last Modified: Thu, 20 Jun 2024 20:17:53 GMT  
		Size: 3.4 MB (3413894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60b90f7561d619b86ba6ab382e19ab049e06aa40685f71b1534233f0fea8643e`  
		Last Modified: Thu, 18 Jul 2024 00:55:31 GMT  
		Size: 100.1 MB (100123815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u422-alpine3.18` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:d94c930d2b4f2c5a5f343e65c48158776545b5b91ad9353a13cbb702625d1132
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.2 KB (254228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62ec8de6fb5036641fde0d04c0ac6811c5c18cd588a4c3eb914fabd39c9b4d4e`

```dockerfile
```

-	Layers:
	-	`sha256:65ce0ff5367ba315170322eb3731b4d5192613a6b9f964bd0ce82a17e4a33bde`  
		Last Modified: Thu, 18 Jul 2024 00:55:29 GMT  
		Size: 245.1 KB (245075 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef3551ea4083632c6882dfb8c9c9afb38804ba5abd3362e5c033cfb103be874b`  
		Last Modified: Thu, 18 Jul 2024 00:55:29 GMT  
		Size: 9.2 KB (9153 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8u422-alpine3.18` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:dd8ccef4d6b11834ca7e2fcee22e9e8e68cc2a0d4602e4d2afc0b7e6d8cdafee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.2 MB (103173941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5621346e21991e17fc40bb2ca0c0be479bb53ccc5a4044e11209a502a98d380c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 20 Jun 2024 17:40:41 GMT
ADD file:4f760ede9d48d6073317cae6d632deaab101f337e09c56a7f9b8847ed99de3e8 in / 
# Thu, 20 Jun 2024 17:40:42 GMT
CMD ["/bin/sh"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=8.422.05.1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=8.422.05.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 16 Jul 2024 22:56:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:5c905c7ebe2fecec0b1115f145c0ea74b3233aa25d8239903194f6b4424044ce`  
		Last Modified: Thu, 20 Jun 2024 17:41:31 GMT  
		Size: 3.3 MB (3337949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c04b30fdfb8a5255460d6460daf4c158b9475d10c9984ac2c27ba122288c493`  
		Last Modified: Thu, 18 Jul 2024 00:59:33 GMT  
		Size: 99.8 MB (99835992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u422-alpine3.18` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:e2b9bf2bea95157d02935c597d3ec8889cc107b97c7a8e3c50a1fd2756db6522
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.7 KB (254658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d40003049117436760222466945828014dfec178f9d0c66815d52332d2ac023f`

```dockerfile
```

-	Layers:
	-	`sha256:ffae89ce09131de33b80f9bc0464e730a64b0349082171a4d580eca52f94135e`  
		Last Modified: Thu, 18 Jul 2024 00:59:30 GMT  
		Size: 245.2 KB (245207 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7befc2a83a7371f9b8976247ea52392046b4ac34551cba3251f7532e04be242`  
		Last Modified: Thu, 18 Jul 2024 00:59:30 GMT  
		Size: 9.5 KB (9451 bytes)  
		MIME: application/vnd.in-toto+json

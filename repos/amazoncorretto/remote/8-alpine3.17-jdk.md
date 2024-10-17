## `amazoncorretto:8-alpine3.17-jdk`

```console
$ docker pull amazoncorretto@sha256:e1d13ed6e821e99ce1d9ecd6f666e971963e1ca1172f317713d525e9d33bad68
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-alpine3.17-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:6607032ea92949757d0ec5e7f3d887013cfd5dbf2b91111729fd6ccfee366665
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.6 MB (103589369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:266121e8ad2ef29b23bddf3d00b07946e593b66247d1f9f0c4cfd493f40ab20b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:24 GMT
ADD file:8bf458f5fbed9f27c897506538c02fb5810b70aba850bb883d2120985fa15bac in / 
# Fri, 06 Sep 2024 22:20:25 GMT
CMD ["/bin/sh"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=8.432.06.1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=8.432.06.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 16 Oct 2024 02:18:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:a0f4cbe03b6df9e61ce02b3c41bbc05481842858bd48d9687614abe719303b47`  
		Last Modified: Fri, 06 Sep 2024 22:21:07 GMT  
		Size: 3.4 MB (3392194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44f5366820327932cc325302de41436f573a624e280f97efdd205dec5de8f9b3`  
		Last Modified: Wed, 16 Oct 2024 17:55:57 GMT  
		Size: 100.2 MB (100197175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.17-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:7dd0385a6037e66dee28c9a313253135160336240d59339658a31a23c20053e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.7 KB (253721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c33071f6cbf3a84205b1aadd0f20a396ddabbf139843fe57f3626c47bf74f0d`

```dockerfile
```

-	Layers:
	-	`sha256:8b0040c712bd1be006861deccde821b216c1fb5150c7f8f7bb78979db0232f9f`  
		Last Modified: Wed, 16 Oct 2024 17:55:56 GMT  
		Size: 244.5 KB (244530 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85fcf18e102679d83b39365984282d20e5e626a7b96d8340c783de4d2dcb1992`  
		Last Modified: Wed, 16 Oct 2024 17:55:56 GMT  
		Size: 9.2 KB (9191 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-alpine3.17-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:6205c6c64f2dd33c68db2c3022a42cde8beca5073788c3aca78ba17bde63a29b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.3 MB (103253965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5946f7fa0733da9ef7973e07dec3c7e7acfbeb54875a8b394d0514089844ffef`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:24 GMT
ADD file:e3f989df31d7e2d820078058c5d0ed7d98695c5b86bd172276270ebb59d75ee6 in / 
# Fri, 06 Sep 2024 22:44:24 GMT
CMD ["/bin/sh"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=8.432.06.1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=8.432.06.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 16 Oct 2024 02:18:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:4a3d188841b4b0359cda0d73dc5f89f8bc569f3bcb178cfd0507b4ead0db7bf4`  
		Last Modified: Fri, 06 Sep 2024 22:45:06 GMT  
		Size: 3.3 MB (3275072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caa8cde40339a8e86ccabf163a25fda4db5a12970751b093d2452f57d74653b5`  
		Last Modified: Wed, 16 Oct 2024 22:02:02 GMT  
		Size: 100.0 MB (99978893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.17-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:5287914e60ead956c13a661f6344b6d718ec8012ebbbb29044551400aae8fd27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.9 KB (253950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ba990060145d0c4d6bc364e0e474b3998c0e7510b95aa14e45ffc6d52fe969b`

```dockerfile
```

-	Layers:
	-	`sha256:380c764d417b67eb5aabe41fb2325a257bcf9f58a0f6145df63c0306c0a26867`  
		Last Modified: Wed, 16 Oct 2024 22:01:55 GMT  
		Size: 244.7 KB (244662 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e7b113e96ee9382c289186a62cc2eab490b1c46d5c726a18ec73270337fb330`  
		Last Modified: Wed, 16 Oct 2024 22:01:54 GMT  
		Size: 9.3 KB (9288 bytes)  
		MIME: application/vnd.in-toto+json

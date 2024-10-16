## `amazoncorretto:17-alpine3.19`

```console
$ docker pull amazoncorretto@sha256:753dadfc02f7a4bd99943cb22532dba3e80b56e3d43958afcf4d4faaedef5578
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-alpine3.19` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:6bc056cd7b06bbb0e8964b2c23baa6be4635f8de0e60fcac046e84a7db44ea53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.1 MB (149069258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:522fac954ec16b45a3dba93f0a24dc4822d7fc63748b82e1e8b3353e20a1646f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:13 GMT
ADD file:9e193d6fff4bce11c0ee715ad87def9ef40e9608d4be84cf73391edd45b2810e in / 
# Fri, 06 Sep 2024 22:20:13 GMT
CMD ["/bin/sh"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=17.0.13.11.1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=17.0.13.11.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 16 Oct 2024 02:18:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:94c7366c1c3058fbc60a5ea04b6d13199a592a67939a043c41c051c4bfcd117a`  
		Last Modified: Fri, 06 Sep 2024 22:20:51 GMT  
		Size: 3.4 MB (3419706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b0e4654439aa41edc4dc74c95e9ed5b17587a49dfcbc5bf7d19fd7d3a5fbde1`  
		Last Modified: Wed, 16 Oct 2024 17:57:23 GMT  
		Size: 145.6 MB (145649552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-alpine3.19` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:2310f28638078ee3fb583047a32823da9fb5fb5cdff980fc8dba514a8e67d32a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **390.6 KB (390646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f44cb6498b9af4ec62db0dc2f279c9db4c5b71ca77524ae30ef572e59ad288ff`

```dockerfile
```

-	Layers:
	-	`sha256:5d1af48f3172cc1c767468d0449f31a53b891cea2543b7ec251789d1276d1021`  
		Last Modified: Wed, 16 Oct 2024 17:57:19 GMT  
		Size: 381.4 KB (381431 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1fbb8c76cae69e9315f21b655cafe98635492364ff87655ac9e23414bc629d88`  
		Last Modified: Wed, 16 Oct 2024 17:57:19 GMT  
		Size: 9.2 KB (9215 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:6ae421a6d4e5cc8dc5155992a87d04acbfdd00cecfb59949a8f2978806c7b5ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.3 MB (147294267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d56946c6d82f96ddcddc26b256cde29dfc57f7c64cbbb4e564c77569f59fcc49`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:16 GMT
ADD file:9865d69f45511580cc2a05d8a9573251b6eb5a84520efe2e8295532e3ccd6321 in / 
# Fri, 06 Sep 2024 22:44:16 GMT
CMD ["/bin/sh"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=17.0.13.11.1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=17.0.13.11.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 16 Oct 2024 02:18:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:188a7166e45935ced07634efdc8e63c13f5f7673b60b051b353475ee00e28fe0`  
		Last Modified: Fri, 06 Sep 2024 22:44:50 GMT  
		Size: 3.4 MB (3359103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b14d02fba89363190724728cce94477c9ac8dc8143b677d29ba929a7cc3d6f3`  
		Last Modified: Wed, 16 Oct 2024 18:29:58 GMT  
		Size: 143.9 MB (143935164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-alpine3.19` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:a5b46edf420574261cf357240efe750aa64510a82d8342d4ba483590d10bfd20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **390.2 KB (390162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e68c99a38a4e4afd7df5c4e03037aa7a460035e9985255a84d9962500765b84`

```dockerfile
```

-	Layers:
	-	`sha256:3c7b0dc2fd7befc868c068111627d738b935821e5a94cfb4c527d9b7a1ed269e`  
		Last Modified: Wed, 16 Oct 2024 18:29:54 GMT  
		Size: 380.8 KB (380849 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7977535722432fbda18b216c69ca7f4f86cd48e729f591ded9076b8651ac99e`  
		Last Modified: Wed, 16 Oct 2024 18:29:54 GMT  
		Size: 9.3 KB (9313 bytes)  
		MIME: application/vnd.in-toto+json

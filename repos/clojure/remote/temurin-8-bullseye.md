## `clojure:temurin-8-bullseye`

```console
$ docker pull clojure@sha256:bc039d98004826473f4dc1b31c8d97e39ee01a44c7b7f52ddffe19d3e6bc3dc2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:13725a52de5290f74a4f9d08f5dc452e9ef71415c79df42fa2e820fdb93d7ad2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.7 MB (177651720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16c34055da09d9f6922fe4069e304f1e1ce2143c7993f24dc4ea55f056c4fdb3`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 29 Jan 2025 19:11:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1738540800'
# Wed, 29 Jan 2025 19:11:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 Jan 2025 19:11:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Jan 2025 19:11:46 GMT
ENV CLOJURE_VERSION=1.12.0.1501
# Wed, 29 Jan 2025 19:11:46 GMT
WORKDIR /tmp
# Wed, 29 Jan 2025 19:11:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "65257085958376a3c89755a6108d67163882c75af709fe8c8918222ca5730aef *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:478cb73646107d7b3f891aa53abaed926667463844c07b1d924bd760ae03f38a`  
		Last Modified: Tue, 04 Feb 2025 01:36:37 GMT  
		Size: 53.7 MB (53738873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0615cdb1f0e4320384c5d4d6eb2f0e5111f1a0165c6d6ca0995a53d282adee5`  
		Last Modified: Tue, 04 Feb 2025 05:28:00 GMT  
		Size: 54.7 MB (54721284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa58f07f115cbe7da3e858822166ce193a82c53a69f55dbe1df45a2bbc997f41`  
		Last Modified: Tue, 04 Feb 2025 05:28:01 GMT  
		Size: 69.2 MB (69190918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16fe94bda56b0ae7ec709c064ff1fea76cd92f46acc3ad790789acc5f5982327`  
		Last Modified: Tue, 04 Feb 2025 05:27:58 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:96c5be131c10013126a91babc01a85211391ef8281bb4b23d44eab377cd07c97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7340402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b88e0c1f8b748f58bdcfd1e22ef5d5174bead954242e4904d6e5eb078f6e6918`

```dockerfile
```

-	Layers:
	-	`sha256:3bc5d1402cfbfd79ce665bf302984cb7521cb644649743cec06de1bbfb1bf0cf`  
		Last Modified: Tue, 04 Feb 2025 05:27:59 GMT  
		Size: 7.3 MB (7326165 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a62659ca740a009d551edf193a3044c160dc8a5b69a0553f6a66a9955b72c167`  
		Last Modified: Tue, 04 Feb 2025 05:27:58 GMT  
		Size: 14.2 KB (14237 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:5fb77d7c2879d2856ef6fb27a91ae23aab0f8f23ed656a8cc7e2bdd404f1e3c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.4 MB (175380457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:350c84ef1d2a33b2de7e8a2bb3ea07c1322ec5221ed90b507cb329fbbefdc28c`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 29 Jan 2025 19:11:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1738540800'
# Wed, 29 Jan 2025 19:11:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 Jan 2025 19:11:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Jan 2025 19:11:46 GMT
ENV CLOJURE_VERSION=1.12.0.1501
# Wed, 29 Jan 2025 19:11:46 GMT
WORKDIR /tmp
# Wed, 29 Jan 2025 19:11:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "65257085958376a3c89755a6108d67163882c75af709fe8c8918222ca5730aef *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:0038ef039a89ede34c57806e684dc9d9be7dcd22d3c08b90deb36bb22a2c7122`  
		Last Modified: Tue, 04 Feb 2025 01:38:11 GMT  
		Size: 52.2 MB (52245695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef7e26da71c068cb6c68e55199cec0b81f2ef30055e49e4a653cd41241402103`  
		Last Modified: Tue, 04 Feb 2025 23:25:54 GMT  
		Size: 53.8 MB (53822761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8611f35d8ee92ad96bd926d6a53f1139196691538921fb80a60e9de3246268d`  
		Last Modified: Tue, 04 Feb 2025 23:30:31 GMT  
		Size: 69.3 MB (69311357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4876071eb62b073d0b0063cf7a7b735576eb354ebdc5dd70090165c2a4e6bf62`  
		Last Modified: Tue, 04 Feb 2025 23:30:29 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:eb6d320e1196faf5c3e44578f15a772648b78dfbb4f42707d39af78968e526de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7346315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c59f8e0ade849b0a1eb7782c63d8b54d39e9e5ed983df7910d225f9f0f9c1059`

```dockerfile
```

-	Layers:
	-	`sha256:f22e0c1cb4b6529fd73080b131bd10375294ab884e3fb5089024b36006c2117e`  
		Last Modified: Tue, 04 Feb 2025 23:30:30 GMT  
		Size: 7.3 MB (7331962 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c713810c78d0742f54da9cdef80592d7131e78aaf8abd507420c09223f1465b`  
		Last Modified: Tue, 04 Feb 2025 23:30:29 GMT  
		Size: 14.4 KB (14353 bytes)  
		MIME: application/vnd.in-toto+json

## `clojure:temurin-11-tools-deps-1.12.0.1501-bullseye-slim`

```console
$ docker pull clojure@sha256:09f1b7b6655a8f3c3a95f71d0a6c3b9f36d5cadb8a999d21e1a09240f186caff
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-1.12.0.1501-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:4d69cf8e6b68aa828013495fbf966f6e9da928055659ef5662415593b1e45cd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.6 MB (234642625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc2e76e0ea4329860d6e23b4b3cb9025c030b7fad6008268768dfcdd6ffd4263`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1736726400'
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
	-	`sha256:89320e7119e225692d79aaeb4989a18d7f97daafdb2b3782f84a0a8de31a09de`  
		Last Modified: Tue, 14 Jan 2025 01:33:29 GMT  
		Size: 30.3 MB (30252665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d3e8ee7f3fcbcd89378f73f5d0ece0074805216af35892f27d2d88144d649e6`  
		Last Modified: Wed, 29 Jan 2025 20:27:32 GMT  
		Size: 145.6 MB (145601449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4135e929b97c1ead14c4865b29f4ed839f7715feac75a98cb2555d61a6f407c9`  
		Last Modified: Wed, 29 Jan 2025 20:27:31 GMT  
		Size: 58.8 MB (58787867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5925d7a31121d47e1a749570c0dbde668926970f213247cbaa0413a0aa167273`  
		Last Modified: Wed, 29 Jan 2025 20:27:30 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.0.1501-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ae9d44d1405051a364436a032303596828d051cdc33449fc99dd97c8c745a2cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5151517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53e7b83bf101265e3bdbeeed41ebf7d2ac7294f83b5544135c9d8b751e8b22f6`

```dockerfile
```

-	Layers:
	-	`sha256:af52d77c9284e9eaa3cb8f2aefa0e8afe54a78b8f29a9b4d9b135cad65ae7ca6`  
		Last Modified: Wed, 29 Jan 2025 20:27:30 GMT  
		Size: 5.1 MB (5137208 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:69ee38449a5983c474cc89dc14e57eb54b29e14b967d7dd4f82df3637865ac1d`  
		Last Modified: Wed, 29 Jan 2025 20:27:30 GMT  
		Size: 14.3 KB (14309 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.0.1501-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:aca61296f65ebea1960641f1bf867731aa35e292efcf4447f0a7253ff8ff533a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.0 MB (230044265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d74cdf187c39e1a8f40e26ae72673157a0a1351ee5fc06ec4099bcc4e636c84`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1736726400'
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
	-	`sha256:6a43d3167ec1fb9f3b40bf3e095c86abebf31d406e2de1d196433c26d262f72c`  
		Last Modified: Tue, 14 Jan 2025 01:36:26 GMT  
		Size: 28.7 MB (28744913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50e7318fc7b6adc75e412ca84446f8d4b328fe39f5b4007bd252c5f5158a3fd0`  
		Last Modified: Thu, 23 Jan 2025 00:51:23 GMT  
		Size: 142.4 MB (142389489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2138555dbefb8bcd8650717f2eedd4b20ecf3116eb4065da3b07cd49a2219a8d`  
		Last Modified: Wed, 29 Jan 2025 20:45:49 GMT  
		Size: 58.9 MB (58909218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9e808d1bda3a6851650e283817b854c49982394ffe933ef790a4cc17ecb5593`  
		Last Modified: Wed, 29 Jan 2025 20:45:48 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.0.1501-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:fd7f9750c39ee60c9d55723ceb92837ca333fec16102a2789c91552742c0e921
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5157986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76ee1ec06d2ff32bf03589c02b7912be70971bad2654dba4b57beb508e2e20f4`

```dockerfile
```

-	Layers:
	-	`sha256:c96a05ce6d009d0795f7b45809f53b0ee1b4c2cd2238aa5ecf0d359099c47b10`  
		Last Modified: Wed, 29 Jan 2025 20:45:48 GMT  
		Size: 5.1 MB (5143558 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34c0df87acde3cc6f33893c9f3eac21500be1774a7d6967245af6e809983e844`  
		Last Modified: Wed, 29 Jan 2025 20:45:47 GMT  
		Size: 14.4 KB (14428 bytes)  
		MIME: application/vnd.in-toto+json

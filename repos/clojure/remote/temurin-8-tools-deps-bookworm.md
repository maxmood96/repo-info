## `clojure:temurin-8-tools-deps-bookworm`

```console
$ docker pull clojure@sha256:33b1948b81a90382f7c047143fb0648373e1ebd47d678216b9145c896865f09f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:68136a645a9975cc8e4be0f88106d791f43485d02c16506a1690413f2a9ea72a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.1 MB (234095750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91c7e533b1ac97c132b97c8c0a1996360d15dbe042aa78d58418a82d32ae7416`
-	Default Command: `["clj"]`

```dockerfile
# Fri, 27 Sep 2024 04:29:19 GMT
ADD file:087f68d5558e06c7160c9322582925635e7539a7702413828357c28c77f6f345 in / 
# Fri, 27 Sep 2024 04:29:20 GMT
CMD ["bash"]
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:cdd62bf39133c498a16f7a7b1b6555ba43d02b2511c508fa4c0a9b1975ffe20e`  
		Last Modified: Fri, 27 Sep 2024 04:32:50 GMT  
		Size: 49.6 MB (49555051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4a73abc6b4ee458b17cb245a6712d4d776c258d1dd260dc50ea86cb566eaca1`  
		Last Modified: Wed, 16 Oct 2024 16:12:52 GMT  
		Size: 103.6 MB (103611910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17d3450c2a83c0d631da57c88c53f7c0d1e441b2cf9a0db7aefaa4c48ed401bb`  
		Last Modified: Wed, 16 Oct 2024 16:12:50 GMT  
		Size: 80.9 MB (80928144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff747307fdc951865af66dfc5c2abd8cdc07c7080ac0599fcd4d71f81f35c6dd`  
		Last Modified: Wed, 16 Oct 2024 16:12:49 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:b1b5900ce4a83ba25e4287bb00af958e97916c94bc0c1d6c6ec1cddac57239c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7292702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa0bcf81da8da13cf270e1a818db6c551a8afbe254496a648acc7f17e633a71f`

```dockerfile
```

-	Layers:
	-	`sha256:44ee811ef6463680cebbd589077c890ff605347952905f21da01b4448cb0f748`  
		Last Modified: Wed, 16 Oct 2024 16:12:49 GMT  
		Size: 7.3 MB (7278812 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31c284e3fe97e5df305ac2852487154953f2a161209a8f8b1ad5809b2941d05f`  
		Last Modified: Wed, 16 Oct 2024 16:12:49 GMT  
		Size: 13.9 KB (13890 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:9eaa4453cd4cd3d29ec4e464b2bafd194e1444691e56105c264ee4da52d6b913
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.1 MB (233105259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2796d26479b17e024708b3350c67a4b20489ca917c9a3b9c9cb47d9adb3660a0`
-	Default Command: `["clj"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:09 GMT
ADD file:e689b230a6f8e5eb3500dfa6f80afd8bda70b82deda3656ddeea10df15dd54c3 in / 
# Fri, 27 Sep 2024 04:38:10 GMT
CMD ["bash"]
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:6d11c181ebb38ef30f2681a42f02030bc6fdcfbe9d5248270ee065eb7302b500`  
		Last Modified: Fri, 27 Sep 2024 04:40:33 GMT  
		Size: 49.6 MB (49584886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38ecad2787dcca3a8c8c0ea14fbf45ecfb2849534e875dddde4d908bdbb9afd8`  
		Last Modified: Sat, 12 Oct 2024 00:55:51 GMT  
		Size: 102.7 MB (102729218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0382f1ece06cff8f449738b81af5ac8c222cc9ca403c75f01eb11a3ce047dd5`  
		Last Modified: Sat, 12 Oct 2024 01:00:31 GMT  
		Size: 80.8 MB (80790513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d388ee2c6fb16a40fd8412174408d19af6f902443c71ae0eee798bb45acb288`  
		Last Modified: Sat, 12 Oct 2024 01:00:29 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:f52a4585ba38390119c99706e7b19e892ed744099c0917f3ec1c57c424a89de5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7299273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:696603a40c7395f2ce9049d362ce65e89e44fb833d6138a5d1e735a5409f8838`

```dockerfile
```

-	Layers:
	-	`sha256:77f9082e3caac2340acc843701f956e95f8cdd1ccd4711f80ce3002037cb7fb3`  
		Last Modified: Wed, 16 Oct 2024 02:07:47 GMT  
		Size: 7.3 MB (7285279 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6744add1bca453582e303f20a8e413ec2885619e5f2e0637064e874c856af367`  
		Last Modified: Wed, 16 Oct 2024 02:07:46 GMT  
		Size: 14.0 KB (13994 bytes)  
		MIME: application/vnd.in-toto+json

## `clojure:temurin-8-bookworm`

```console
$ docker pull clojure@sha256:d596180a71d827664c8c4e6834ef31ee0b5c4caedd56223a7cf6b59508f8cdf1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:08741ee4675c9a958f7c61766c8d388132b8fc98786622ad2686da508b72e64e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.1 MB (234095713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8069865c1ec3be321fa3f9201daa4a8868a5b1563953210519390f5e57066a3b`
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
	-	`sha256:d650bf5f4959e0ff71b6b064903fd82c5f1cd1b92b2b79c11d156a5403baa054`  
		Last Modified: Sat, 12 Oct 2024 00:53:32 GMT  
		Size: 103.6 MB (103611902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7085656a8e466052292bbf35037c4b4e010bd7293cfd661d32975a3e4dbcc9e1`  
		Last Modified: Sat, 12 Oct 2024 00:53:35 GMT  
		Size: 80.9 MB (80928115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f165f936487de1cab126daa5d5734d9612e4e90a0955bd3781c1a8102211cb33`  
		Last Modified: Sat, 12 Oct 2024 00:53:34 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:1b1e7ba5f36c63d70d5f5c18d38dee87ac038b0391fe02e0cc3b5ffcade25f92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7292702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cd0edc6093774d59f8258ffa69b5b499c6bbc77ffb50dcb0a39ba5ca94c90f7`

```dockerfile
```

-	Layers:
	-	`sha256:eac0c8aaf31e170427602ebd3821a5005ff27988c289778ba8c61896a676bb69`  
		Last Modified: Sat, 12 Oct 2024 00:53:34 GMT  
		Size: 7.3 MB (7278812 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d3152753d0d96ec5ae95927f2502363254c49423b23e5138d694951e50c44f7`  
		Last Modified: Sat, 12 Oct 2024 00:53:34 GMT  
		Size: 13.9 KB (13890 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bookworm` - linux; arm64 variant v8

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

### `clojure:temurin-8-bookworm` - unknown; unknown

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

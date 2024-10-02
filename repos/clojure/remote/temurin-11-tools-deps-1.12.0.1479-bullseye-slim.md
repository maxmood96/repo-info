## `clojure:temurin-11-tools-deps-1.12.0.1479-bullseye-slim`

```console
$ docker pull clojure@sha256:c8338c55e5ee0162bfa5f22a9a94fda79be8e64b8adbd2308c3e192f9532c9c8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-1.12.0.1479-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:63b613d909bbff6ef6190d8d4ac603cb67a09659b3a46030fec785b669fca68e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.9 MB (235919144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:733ec9a304053150e4d05fa8ad00318e468c02853b52a7dc5ad3de30b703c195`
-	Default Command: `["clj"]`

```dockerfile
# Fri, 06 Sep 2024 16:59:26 GMT
ADD file:270cda9833ffe6dfbe916662a9204a205f41c1fd440b66ec822ac00de86a5f5e in / 
# Fri, 06 Sep 2024 16:59:26 GMT
CMD ["bash"]
# Fri, 06 Sep 2024 16:59:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 06 Sep 2024 16:59:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Sep 2024 16:59:26 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Fri, 06 Sep 2024 16:59:26 GMT
WORKDIR /tmp
# Fri, 06 Sep 2024 16:59:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:fa0650a893c25858ebb09921bc9b7824594e23405374a6adbcd3b4e27e28e3cf`  
		Last Modified: Fri, 27 Sep 2024 04:33:50 GMT  
		Size: 31.4 MB (31428599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aefef277d5cf50fe89a8c400cdc5509211b3165ea21c59ee765c1c2733f7a67c`  
		Last Modified: Wed, 02 Oct 2024 02:57:52 GMT  
		Size: 145.5 MB (145549818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:225cef9fab7362c1fe3a31934a33b10e1b1e4aa6b4848918cc0ef387c08db725`  
		Last Modified: Wed, 02 Oct 2024 02:57:50 GMT  
		Size: 58.9 MB (58940084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd545ccad85eadcba19ec42ba3487f0f2737f814eeaf5be1b737884f316194b6`  
		Last Modified: Wed, 02 Oct 2024 02:57:48 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.0.1479-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:5637f4f6d086da82cefd44c37560cbf688982aee793d31a501a7c1253c59ee78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5133595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7145c18d911343b682ed333b141ad7763903a9800a09d2e9df8ff63d5ed04142`

```dockerfile
```

-	Layers:
	-	`sha256:40c7364bb64c9b776977f78fefef643453d6a980fa5c38a580759130a61f5b94`  
		Last Modified: Wed, 02 Oct 2024 02:57:49 GMT  
		Size: 5.1 MB (5119652 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7240f8e34507302a083a19f49c095a29e9a99ca8c2c545560b7b651699df4a94`  
		Last Modified: Wed, 02 Oct 2024 02:57:48 GMT  
		Size: 13.9 KB (13943 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.0.1479-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:22ac58e46c64876c49e634b49e1d553b34d016ec612a4ea43a80f6771ef4eecc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.5 MB (231503932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd57201d171ac953bbbd11295ae6a9f089c0e6a07fd90061b4f171b5fe6b53e0`
-	Default Command: `["clj"]`

```dockerfile
# Fri, 06 Sep 2024 16:59:26 GMT
ADD file:a981209c874e612fdb9f74c3315954986cfdc61cf22ab48477f2e96b3e7aeedf in / 
# Fri, 06 Sep 2024 16:59:26 GMT
CMD ["bash"]
# Fri, 06 Sep 2024 16:59:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 06 Sep 2024 16:59:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Sep 2024 16:59:26 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Fri, 06 Sep 2024 16:59:26 GMT
WORKDIR /tmp
# Fri, 06 Sep 2024 16:59:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:2245c7c084558dcf55e2bad9579c63dfdbd831cdbed2e063a1c25322cb793bed`  
		Last Modified: Fri, 27 Sep 2024 04:41:27 GMT  
		Size: 30.1 MB (30075158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30149fff09dc33f83b6ab4318fbe4dd4f83df2dc3e54bf33b92b83879e58b67b`  
		Last Modified: Wed, 02 Oct 2024 02:12:34 GMT  
		Size: 142.4 MB (142354841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d74861c9197d2d977035c28c9f32801184a03d7cc9b39e8d2055e080ad5c2663`  
		Last Modified: Wed, 02 Oct 2024 02:16:47 GMT  
		Size: 59.1 MB (59073290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a223ba140acd6ff0a2f3001cc493a9b651bd263c10ea0876d77220c8ad741ad`  
		Last Modified: Wed, 02 Oct 2024 02:16:45 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.0.1479-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:874c1acb6530893aad62cd58339a34ead94d2684b1c16de9a7a6894b4db8f423
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5140057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bd378a6bb68443df072ac0398cf0474f7b581e0ef44c6157e2e671883aeb82d`

```dockerfile
```

-	Layers:
	-	`sha256:70c126221b921f1877d7704a767a672ee064ddcd12d1db71c1e3a48016388824`  
		Last Modified: Wed, 02 Oct 2024 02:16:46 GMT  
		Size: 5.1 MB (5126008 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4df4d40e0ef83ea603c1f76134ca8ed550f3b96dd58fe90340d44b2d03fd0508`  
		Last Modified: Wed, 02 Oct 2024 02:16:45 GMT  
		Size: 14.0 KB (14049 bytes)  
		MIME: application/vnd.in-toto+json

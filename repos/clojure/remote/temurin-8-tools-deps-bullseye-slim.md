## `clojure:temurin-8-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:7ef24c2508859a14c55a736bb311322c6906d8a470d53b5e959259afec603fb3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:831158b0a59547b1ddc830294c81a882bad9de9012c580dcc853068d48322bdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.0 MB (193981330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca056ba43763e2e969e44fc28c898e16b8d7f67b716cf740b2b822777c50caac`
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
	-	`sha256:61bbce6e2ba66c6eb5b0f38c9f7e7a0993fd904a51bcf81cf83aed67011c4ad5`  
		Last Modified: Wed, 02 Oct 2024 03:56:35 GMT  
		Size: 103.6 MB (103611880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:300eb3d44c44db47c590819c51d099781aa36c6fb2451e0442c483e57057a96c`  
		Last Modified: Wed, 02 Oct 2024 03:56:34 GMT  
		Size: 58.9 MB (58940206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5289ca2c3dfc6df46d5abd2b6898ebda1bcf0125faca5e087776cf001c600d8d`  
		Last Modified: Wed, 02 Oct 2024 03:56:33 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:5769816c098232146d443e313c404c081206ae5bcc592f2857f312ca2f89535d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5235577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34b289aced78c5864406a4d090ac12e3907af01377e6c104c00bf47a76b001c5`

```dockerfile
```

-	Layers:
	-	`sha256:4d801a489b5dd4fd56c696e1275b3b40927747c0d618843784925200f96e3030`  
		Last Modified: Wed, 02 Oct 2024 03:56:33 GMT  
		Size: 5.2 MB (5221651 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f689dfa149218df9c03e0a0b01482556db86845851081981baab4b27c0b1b013`  
		Last Modified: Wed, 02 Oct 2024 03:56:32 GMT  
		Size: 13.9 KB (13926 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:fc9bcedbd5d218c96e723d379062d949639fb6fb7ad050d67390ca473e4bfd38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.9 MB (191878210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5ca5a74d72a8eeed483f2869b9c1b594e1ca36ea5f6b09c44a5626a839e32fd`
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
	-	`sha256:73cc39bffd576a347f677dd7df7ab9c14e7fd641e1f0138ca52465f8f346536c`  
		Last Modified: Wed, 02 Oct 2024 05:28:33 GMT  
		Size: 102.7 MB (102729197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c201c715b947d5252bca684cb3a9dfeead1baede974be60a721a50a3eaeefd18`  
		Last Modified: Wed, 02 Oct 2024 05:33:27 GMT  
		Size: 59.1 MB (59073211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51cf615a470fc60354e3397ad209d549f8d88ec44016b38366e97cb1314a2760`  
		Last Modified: Wed, 02 Oct 2024 05:33:25 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d8c8c5be976dbc94d15552b0abdbdec159f91c7d4c1531b56767d8689774a611
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5242119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0c56ac289592e5da269cf8907cc9d50bc4ce45507959a3c952a65d594e7a229`

```dockerfile
```

-	Layers:
	-	`sha256:edaa99f571b15201f6e0c77bc57c1fd61caf7f7362ed01abe77c3331674a8a3d`  
		Last Modified: Wed, 02 Oct 2024 05:33:25 GMT  
		Size: 5.2 MB (5228087 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9242bb486205e585a1dcf13e8b3085947693c2235cdd191f64d57919714c1cb8`  
		Last Modified: Wed, 02 Oct 2024 05:33:25 GMT  
		Size: 14.0 KB (14032 bytes)  
		MIME: application/vnd.in-toto+json

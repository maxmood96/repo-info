## `clojure:temurin-11-tools-deps-1.11.3.1456-bullseye-slim`

```console
$ docker pull clojure@sha256:514fd23e849e6cdd3853e37d57696b3e66318e37b142d696be9ee93bdf26f43d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-1.11.3.1456-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:a4fe90dee28a7b295d43d80d5f869cd7bb4bf4acd42a66aa3020836341c5d78f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.6 MB (235552524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5e20873f6bd31155a4911652409b6462578869bd69d795ccee29339c1123219`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 28 May 2024 15:17:11 GMT
ADD file:49759b7a74bac875e3619e20ed5a9521101c7729f601d90976d0755d30e97499 in / 
# Tue, 28 May 2024 15:17:11 GMT
CMD ["bash"]
# Tue, 28 May 2024 15:17:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 May 2024 15:17:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 May 2024 15:17:11 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Tue, 28 May 2024 15:17:11 GMT
WORKDIR /tmp
# Tue, 28 May 2024 15:17:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 28 May 2024 15:17:11 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:76956b537f14770ffd78afbe4f17016b2794c4b9b568325e8079089ea5c4e8cd`  
		Last Modified: Tue, 02 Jul 2024 01:29:27 GMT  
		Size: 31.4 MB (31422284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d958f90a1c1ed40757700d96bfcf4ee500afcde861abcbf3fa70793058ec6784`  
		Last Modified: Tue, 02 Jul 2024 03:03:02 GMT  
		Size: 145.5 MB (145505247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46dcf2db239e125609526ff704b0b74dc7580b98befbfaec8d8a01acb8d7c5f5`  
		Last Modified: Tue, 02 Jul 2024 03:03:01 GMT  
		Size: 58.6 MB (58624348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dcc5a1a716a511d2e48eb71ce7169d5faa0967dcd78e41f5f460f0754bfedb0`  
		Last Modified: Tue, 02 Jul 2024 03:02:59 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.11.3.1456-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:3514d154a6b98dcc2c3f34dbb851c2b27735eed3341e89628196a955fc4f5af5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4923208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d59eac5265da2d81b05c73be6536341aa738d58628287a6f55afcdd81efd1dc`

```dockerfile
```

-	Layers:
	-	`sha256:3d4972146d38a4de1a6f8876b3c6f7591c1e5cd16eeb00036b00b39c77bd213c`  
		Last Modified: Tue, 02 Jul 2024 03:03:00 GMT  
		Size: 4.9 MB (4909272 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bbf80fde2e9584a989b4e47ab4dd4027bbff381f50f94a0e08358646c6bb4e3b`  
		Last Modified: Tue, 02 Jul 2024 03:02:59 GMT  
		Size: 13.9 KB (13936 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.11.3.1456-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:5cb4d4b804a96e1c047ae949477198150864832f4af765e38eafd4046c3c3d7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.9 MB (230931826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:253e10b4fdc49d6393579db542920493b2a1bc6bb2d28dd8a4b59e00f70b9c04`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 28 May 2024 15:17:11 GMT
ADD file:55edb70d595bba9782144ef15994a2ae5c40adeb65f6c3acd6570a0c148ffa96 in / 
# Tue, 28 May 2024 15:17:11 GMT
CMD ["bash"]
# Tue, 28 May 2024 15:17:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 May 2024 15:17:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 May 2024 15:17:11 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Tue, 28 May 2024 15:17:11 GMT
WORKDIR /tmp
# Tue, 28 May 2024 15:17:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 28 May 2024 15:17:11 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:ca4da1869379178993d4f7abc946f75e7515789ff7e15c7ccfedfc8e2bfeaf6d`  
		Last Modified: Thu, 13 Jun 2024 00:43:54 GMT  
		Size: 30.1 MB (30086973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5737b1460bc8700dc97acb941195e47f2f3d16b9162522c09d5187556fa3189a`  
		Last Modified: Thu, 13 Jun 2024 11:30:48 GMT  
		Size: 142.3 MB (142304050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0794c5acb4a7a4be257025cd6ae06fa3d1b01debe26cc3c73db14acd5331ae94`  
		Last Modified: Thu, 13 Jun 2024 11:34:23 GMT  
		Size: 58.5 MB (58540154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b788d12b968a713c02f38c0b49061ca606ac1a19b7bbc3d1061a1b863ea8ca3`  
		Last Modified: Thu, 13 Jun 2024 11:34:21 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.11.3.1456-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:108531394cf948c1778717791f9c464dc975ce04449963e5b4107c9e1a627c0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4930065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbe3e8f42f7fb941b08b81a32bf0076e5a2358ef8fa45a545edfe47ec1c50180`

```dockerfile
```

-	Layers:
	-	`sha256:4cbfb1d9a3a15333c6de643f86c5f74adc07742b4167dab72885c53428c4f403`  
		Last Modified: Thu, 13 Jun 2024 11:34:21 GMT  
		Size: 4.9 MB (4915589 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8da074b648789c61b10d6b271fee09dba3deb79d412fe12deaf224b64c4a82f4`  
		Last Modified: Thu, 13 Jun 2024 11:34:21 GMT  
		Size: 14.5 KB (14476 bytes)  
		MIME: application/vnd.in-toto+json

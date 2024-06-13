## `clojure:temurin-8-bullseye-slim`

```console
$ docker pull clojure@sha256:9c7213f7fadd23136183dc538a5dcf786de4ac0bb8703aa56b7646bd7ff4f74b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:ffcd8e4753c037b2df1db32164c0383006f8e73ac8d4db41a4120fd3c53482a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.5 MB (193455112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2ca6b03ddf9f022cc60fe1430dcd1c96eb86329d5a04b63517192963bde9148`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 28 May 2024 15:17:11 GMT
ADD file:574b112227f85a83f5d80d2523398640537475d2a56fa4c622397c466c0b552b in / 
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
	-	`sha256:f7b75fe1f735933f47315080637abf01f87962d47f8636a07ff4535ed7a4a133`  
		Last Modified: Thu, 13 Jun 2024 01:26:15 GMT  
		Size: 31.4 MB (31434040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1991d3cf3913aae9b9345017bdc47a3b777d13ea27e332d6b9e01465f6db1fb7`  
		Last Modified: Thu, 13 Jun 2024 18:13:52 GMT  
		Size: 103.6 MB (103600229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29b712c2a6d890dcc7b098cc9a870b82f3a94525ca572a2c0254e138206b03bf`  
		Last Modified: Thu, 13 Jun 2024 18:13:51 GMT  
		Size: 58.4 MB (58420193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c032c284f66cad8a63b6a3a13304f505ce062fbec5a0ab961ec132f252dd9501`  
		Last Modified: Thu, 13 Jun 2024 18:13:48 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:fb7de406348562a5780f51216448cdd13f1813353b2300e8238a1781fe6187e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4945641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc4d3aa1d7b0421bbeb5f7be2fbeb3666fae087b9df32dae5b2ec483b11aa50e`

```dockerfile
```

-	Layers:
	-	`sha256:250715358ffbef97a3567449aea58c127276fa125c687660ba5488f919abbeba`  
		Last Modified: Thu, 13 Jun 2024 18:13:49 GMT  
		Size: 4.9 MB (4931721 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6bac65e6a342393a9d2b43e337e4d0ab16f0eb154b788e23cdd0c908c00b301`  
		Last Modified: Thu, 13 Jun 2024 18:13:49 GMT  
		Size: 13.9 KB (13920 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:4108a10f42381cd53718f4e8c531943983d120f0c6885c2d0175bf6993697fda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.3 MB (191328065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:497c58908024095393e9fbd9a14e0cf020747d837dedd8109c09c57f5b9154b8`
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
	-	`sha256:63746f18f87c6c5edfb5273077b2d3e8efce93a8af63851a1486eeacee35e18f`  
		Last Modified: Thu, 13 Jun 2024 11:23:06 GMT  
		Size: 102.7 MB (102700390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2e0ca6b96a5e5c31da1ec13f3cc00d7abc9a72a08bae40fd7afa4ee47c5d7c6`  
		Last Modified: Thu, 13 Jun 2024 11:27:25 GMT  
		Size: 58.5 MB (58540052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72db153c5a11c5270f9d96195bb261b4856c1e3b908b36311b2fa471ef682847`  
		Last Modified: Thu, 13 Jun 2024 11:27:24 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ae7d0e54fb0ca563ee663635a3d28be3e058021ff17c051fab415bde9df074c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4952537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14836c68e7c7972e05569fbfb062e2073d747f524514e18b4075f6520e93896e`

```dockerfile
```

-	Layers:
	-	`sha256:28427619180bfa8f2e43f3acbdacfe5519f5d2551538615bb50c5fe587b57b1d`  
		Last Modified: Thu, 13 Jun 2024 11:27:24 GMT  
		Size: 4.9 MB (4938077 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:760d3940cf5ce0779cfb2526563656e37be347a023787a3cc3cbec4e3eb7a11b`  
		Last Modified: Thu, 13 Jun 2024 11:27:23 GMT  
		Size: 14.5 KB (14460 bytes)  
		MIME: application/vnd.in-toto+json

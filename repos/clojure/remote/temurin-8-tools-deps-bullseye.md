## `clojure:temurin-8-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:b8f81f4fdae074894cef90377e81b6a3626ba3a06019d39a5db433e602518d68
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:ad14b1d14b0e722c093be97c03b43343650343fbd7efb6fcb39165a068eabc8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.7 MB (227718362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc73aff62840818d369a104f364655e712fa5782e1a0792d4eb04f5f6133f91c`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 20 Jul 2024 21:06:39 GMT
ADD file:61c91b2a02e0d3deb2364da03241d137acf78345623ae188082e574b043032a0 in / 
# Sat, 20 Jul 2024 21:06:39 GMT
CMD ["bash"]
# Sat, 20 Jul 2024 21:06:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 20 Jul 2024 21:06:39 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 20 Jul 2024 21:06:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 20 Jul 2024 21:06:39 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Sat, 20 Jul 2024 21:06:39 GMT
WORKDIR /tmp
# Sat, 20 Jul 2024 21:06:39 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 20 Jul 2024 21:06:39 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 20 Jul 2024 21:06:39 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:73226dab8db5240a2ddbdbe2fb1f0949a911563a62a3d5de3c8669ae708e88de`  
		Last Modified: Tue, 23 Jul 2024 05:28:11 GMT  
		Size: 55.1 MB (55084578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ce1787856bb1f3114a333eada582e8fb657acf732e0a7322ed3dd864a0eb734`  
		Last Modified: Thu, 25 Jul 2024 19:02:06 GMT  
		Size: 103.6 MB (103611901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a34ffa0b3e85f62db5750e5933f2b2a26b1f4fdbea60033015bda7f91b2b0424`  
		Last Modified: Thu, 25 Jul 2024 19:02:06 GMT  
		Size: 69.0 MB (69021239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab0cdf6e7512a7c4f54b02571b409894d2e6c79e94e5409cd444109166d87543`  
		Last Modified: Thu, 25 Jul 2024 19:02:04 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:853d6697f4d140b963b242874e1da9d8c3ea911b6ac4afc81399b08dd7956da8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7079687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45672d2d06fbf79f5b49774f01a27e051ea092fe1490ac26a78353d4cf285b1d`

```dockerfile
```

-	Layers:
	-	`sha256:8e65b1f6402416e534105015ca4d866d1f26ed7e246b702c0653b0ab1c49fd99`  
		Last Modified: Thu, 25 Jul 2024 19:02:04 GMT  
		Size: 7.1 MB (7065835 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25820bab408acbe2229c42b727cc1a83be743866eeb512c51160114b1641d51e`  
		Last Modified: Thu, 25 Jul 2024 19:02:03 GMT  
		Size: 13.9 KB (13852 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:3b0f79b3571030b75eedf02b84ca91987671c52cec59c9068c386fcf95ae1cfc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.6 MB (225593867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca5b0678ea5ecd22d4e9343ac17121c0ec019cceb64b9d0bb7178f9cee568bfc`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 20 Jul 2024 21:06:39 GMT
ADD file:bbd5c67ed8e7916601bc20e4ce4973720e715d9dcd892ccbd64c1d5de711a38d in / 
# Sat, 20 Jul 2024 21:06:39 GMT
CMD ["bash"]
# Sat, 20 Jul 2024 21:06:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 20 Jul 2024 21:06:39 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 20 Jul 2024 21:06:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 20 Jul 2024 21:06:39 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Sat, 20 Jul 2024 21:06:39 GMT
WORKDIR /tmp
# Sat, 20 Jul 2024 21:06:39 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 20 Jul 2024 21:06:39 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 20 Jul 2024 21:06:39 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:2c9750102c61ce3f4a11c8776dfc892d41a6d4a662d2882e471664dbad58487e`  
		Last Modified: Tue, 23 Jul 2024 04:20:44 GMT  
		Size: 53.7 MB (53729987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfa99483c1e482a8add6863c8a0b9593712934759e22b2e7c3c82f4278324c6e`  
		Last Modified: Thu, 25 Jul 2024 19:09:45 GMT  
		Size: 102.7 MB (102729199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8ce285f3dac1a72f3c1a1516a433caefbc7b3d8d801fed695559a987685e0db`  
		Last Modified: Thu, 25 Jul 2024 19:15:44 GMT  
		Size: 69.1 MB (69134034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bea8f68c6310b612ea4d5be11eeb7105287b8025a8855cb8b1d7d5f61437eae3`  
		Last Modified: Thu, 25 Jul 2024 19:15:41 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:b0f9b25a5835c93096a42dbc4fefeb797ca2eb6054d9e5836ada938a152f6c27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7085944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29c6ddd1524b37fe15966702c7e3949c0ddfd160b58531de6c325a86fc2f942d`

```dockerfile
```

-	Layers:
	-	`sha256:71d8255459dee60fbb611fdb33d8e9782cd75de5eb9f4673ea0b74c429fbdea0`  
		Last Modified: Thu, 25 Jul 2024 19:15:41 GMT  
		Size: 7.1 MB (7071557 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e3f881d892ea9063975ae44e1a6596e107331a6eddd11166fcab4e128e203b4`  
		Last Modified: Thu, 25 Jul 2024 19:15:41 GMT  
		Size: 14.4 KB (14387 bytes)  
		MIME: application/vnd.in-toto+json

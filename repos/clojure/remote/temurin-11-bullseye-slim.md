## `clojure:temurin-11-bullseye-slim`

```console
$ docker pull clojure@sha256:724e9fa2f351f40700aad7d9e6a7ecccca0b7bf1570ebda5c7d8c3f529a93fa0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:2bd094f87799861291f042807bc8fdf5db43e0ca69e087552a58e4561237b7b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.6 MB (235551588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:583313e9be4b0ef166525cfd09d33dc140a4b52fe519aa59ce1a3116128d348f`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 07 Aug 2024 18:04:12 GMT
ADD file:8b272f437a81ca538a72714301aab84c945a2ff3829fd205d401f488514d36a9 in / 
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["bash"]
# Wed, 07 Aug 2024 18:04:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 07 Aug 2024 18:04:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Aug 2024 18:04:12 GMT
ENV CLOJURE_VERSION=1.11.4.1474
# Wed, 07 Aug 2024 18:04:12 GMT
WORKDIR /tmp
# Wed, 07 Aug 2024 18:04:12 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b23a784c048e4a5b1fc4bcddaea07abcf476621a97d98bbf4f4726c3375d6e98 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:82aabceedc2fbf89030cbb4ff98215b70d9ae35c780ade6c784d9b447b1109ed`  
		Last Modified: Tue, 13 Aug 2024 00:24:25 GMT  
		Size: 31.4 MB (31428287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc32252965ec20225f4e9dbab8deb80c2e9d27347fe38462f7af4c772866b0ed`  
		Last Modified: Tue, 13 Aug 2024 01:11:24 GMT  
		Size: 145.6 MB (145550386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce2e647d441bff2a4807be77a188025f51727a339b2d5fb777a95d7624b46a3b`  
		Last Modified: Tue, 13 Aug 2024 01:11:22 GMT  
		Size: 58.6 MB (58572270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cecd8cf58605d5466a4d686ffe8aed7e6ad16c93fb0a24c7887569c38bd6a93`  
		Last Modified: Tue, 13 Aug 2024 01:11:21 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:394fc191fdcdf942567dedb4a5bdde067d1d13f3ece6d29133fada44a3ea7b0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4963764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cf6f92824be6bb9a4fd753ebc3c59bca7035538502173b0e329025818b7b24a`

```dockerfile
```

-	Layers:
	-	`sha256:4487f5c8512bd17576ec4bdbf4eaf0360dce4fa26ff5bb9b4a57f632dc17adfc`  
		Last Modified: Tue, 13 Aug 2024 01:11:21 GMT  
		Size: 4.9 MB (4949826 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a5bec9a9364ea695a24fd9db02a9c1dd8c2e607e18922b921e63fbf1463ec0b`  
		Last Modified: Tue, 13 Aug 2024 01:11:21 GMT  
		Size: 13.9 KB (13938 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:f615bc31835063b8234e486453312978acd4959dd4f811ce81855e9feaa25362
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.1 MB (231132999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c06ea3f49f43979ac260211a60fb9c8f3317d51301a9e20bd727d253fe45d73`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 23 Jul 2024 04:18:06 GMT
ADD file:3727dfc046704936a0b983a317eeb319ebd0fc5e9da310be06a0ca768df723ec in / 
# Tue, 23 Jul 2024 04:18:07 GMT
CMD ["bash"]
# Wed, 07 Aug 2024 18:04:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 07 Aug 2024 18:04:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Aug 2024 18:04:12 GMT
ENV CLOJURE_VERSION=1.11.4.1474
# Wed, 07 Aug 2024 18:04:12 GMT
WORKDIR /tmp
# Wed, 07 Aug 2024 18:04:12 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b23a784c048e4a5b1fc4bcddaea07abcf476621a97d98bbf4f4726c3375d6e98 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:bd2a3a2ed82de858b38215fac995414b3a91eea4cfe087e5f853ec1faa989ba4`  
		Last Modified: Tue, 23 Jul 2024 04:21:02 GMT  
		Size: 30.1 MB (30076083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:703d98cb03d902ce3b5ff22a5a72804461c9414a2c954de6acd58ad3dcab7506`  
		Last Modified: Wed, 24 Jul 2024 11:27:50 GMT  
		Size: 142.4 MB (142356362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a3024cb08762a7d2178aeede0c340fbf1dfb123fbfdcc81fcab5ffdb12e8449`  
		Last Modified: Wed, 07 Aug 2024 20:04:40 GMT  
		Size: 58.7 MB (58699907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5d0e6baba22f241a1e9035b071a4cbc1703716be72f17d16f0dad3ae384c86e`  
		Last Modified: Wed, 07 Aug 2024 20:04:38 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:447ac821df7e79004b663c8ab6b555e18f334c73a0bc3d753dae4a20584a83fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4970660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e93399463423d4c983f45c7b632725b3046680faa472168aa82a341720e20aa1`

```dockerfile
```

-	Layers:
	-	`sha256:9ae311177c713d2094f694097ba15268b1a519dee92663eb9c60567fc24fce88`  
		Last Modified: Wed, 07 Aug 2024 20:04:39 GMT  
		Size: 5.0 MB (4956182 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e513c727e8a8c5b098b5b7a6b0b19c4d0b5bfb66664ae533b344ac383b91ab8`  
		Last Modified: Wed, 07 Aug 2024 20:04:38 GMT  
		Size: 14.5 KB (14478 bytes)  
		MIME: application/vnd.in-toto+json

## `clojure:temurin-8-bookworm`

```console
$ docker pull clojure@sha256:14bbfd83319d1b3ed84478fc174731465e6caecbec612be67cb613df60aadf27
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:03c9d097dc9d4515d2ae9a889293f35cdc8bd8a7b43ed25cd84d5d4a0465d555
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.3 MB (184349874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc6cdabc3898bc5b15939177921327c656442abd10e9f49473e87552e95c6098`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 26 Aug 2025 17:11:52 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1757289600'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:8fb375ec14f3df8b31b70d0216508565ab7264a7e16cac4f8cc07f8eca22445f`  
		Last Modified: Mon, 08 Sep 2025 21:12:37 GMT  
		Size: 48.5 MB (48480610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bdd77f79e0cc3be09bf305acb0701c11df9a5af924f322b0df4366f8f4242d4`  
		Last Modified: Tue, 09 Sep 2025 12:40:36 GMT  
		Size: 54.7 MB (54731283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:370a4f06ac353b1e026908791261888b36ddebad2678ca603f70843aa12c4f1f`  
		Last Modified: Tue, 09 Sep 2025 12:40:42 GMT  
		Size: 81.1 MB (81137337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed83692fe9e611a81d5e2877de6076a39364edc600bfc5c977ec0b32992e9ce6`  
		Last Modified: Mon, 08 Sep 2025 23:08:06 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:32d44a55462421a26a97b8972fe3bda2b6ff376051ccd16171bd866cbdcaf4cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7510737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6edc085339f714fb08c652e63eb046c3534cdd91f04f3557acd8d0ab1bc4d4e3`

```dockerfile
```

-	Layers:
	-	`sha256:69b0f61d8406a823473d590a9dd49852613a68a3ba4a36cbf2a024e0cde92d0b`  
		Last Modified: Tue, 09 Sep 2025 00:45:29 GMT  
		Size: 7.5 MB (7496500 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3fde1d6ef7cb53d42d521e02eafceb498d8e358bc605d18458443f5c1077b7ec`  
		Last Modified: Tue, 09 Sep 2025 00:45:29 GMT  
		Size: 14.2 KB (14237 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:dba5dcdde455a4bebf08262d32689442e4c68bfbf70038d07b357fc580e754fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.2 MB (183220946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5da21b775e85e45966d7f5b0ed98497246805bd22d0ade492bacb3b2c82474e7`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 26 Aug 2025 17:11:52 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1757289600'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:a9331b686701a987bcd276cc69a0f676d471ccda1aa353d2f7fad017f2894cd0`  
		Last Modified: Mon, 08 Sep 2025 21:14:32 GMT  
		Size: 48.4 MB (48359019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61973c75c233e139576e5a58b5f85b63ca9c27a06a02dd007e0ec63e8b098455`  
		Last Modified: Tue, 09 Sep 2025 09:37:38 GMT  
		Size: 53.8 MB (53835637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:753f959f8a57858e1ba8f38042bbe1397196e7e50de241710be096b3bee1488c`  
		Last Modified: Tue, 09 Sep 2025 09:37:42 GMT  
		Size: 81.0 MB (81025647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a49130eac51f2470d1730e3ed6d90d0d55dacc39d26b9e335bdc31cd00e4f63f`  
		Last Modified: Tue, 09 Sep 2025 01:15:41 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:8f67463e301318ae1f38ce7d9e34b2584dafcca73e9e276a1cca6e65c4de66f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7517316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdad706a19a6713c43501d7a056577770cc4e124407f60a01a1edd92f8e53db1`

```dockerfile
```

-	Layers:
	-	`sha256:28566f2777771aade7eafef8d41d99ae2e9857a1c750823b9dc94c05908a83ab`  
		Last Modified: Tue, 09 Sep 2025 03:43:31 GMT  
		Size: 7.5 MB (7502961 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c1561a7d8d7948f70eaa6432f769344dcf52140a24b48b3f4d30b27287e311c`  
		Last Modified: Tue, 09 Sep 2025 03:43:32 GMT  
		Size: 14.4 KB (14355 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:9c08410d294229336aa906cdec3d17f58d65ccb0b6fa18f393cfa4fa9389b42d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.5 MB (191471628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fabd5d4b44ced7125b83c351f95abd9e769239e24122bce275d4d0ddcf5920a`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 26 Aug 2025 17:11:52 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1757289600'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:64b8116dd43c29a2a4aa3131cb4895af0a7267cc5883e3761556e54c369be9af`  
		Last Modified: Mon, 08 Sep 2025 21:22:08 GMT  
		Size: 52.3 MB (52326822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a7e1fda3375f21ef1250fe439fa1ccdb10e051bc01f9096828ac6125007aa7d`  
		Last Modified: Tue, 09 Sep 2025 08:49:08 GMT  
		Size: 52.2 MB (52165368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10192cbfeb442695bf772ccdc43c1f56ed799098909bfbd10a6c5a9de1478f74`  
		Last Modified: Tue, 09 Sep 2025 08:55:53 GMT  
		Size: 87.0 MB (86978791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:754425367ec066cb5e4011a91505c0b942be6951501c357996b574ed8bb55ac2`  
		Last Modified: Tue, 09 Sep 2025 09:13:32 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:c5a3fc752ee929311b186e62fb41441b616fef5361f49960b3fd24c06ac02330
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7516592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b61d2a3cfa4e682f968df32818b094cac017ad40928bfa08d33b112ffc75394a`

```dockerfile
```

-	Layers:
	-	`sha256:cce17e1a8772b020d7d42b6721e20ee05607376eeeefc5a9df092d7f0ddd7773`  
		Last Modified: Tue, 09 Sep 2025 09:37:12 GMT  
		Size: 7.5 MB (7502307 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce6a27b3a3c686a43392f89749e9a2e55ec7f664c31132201fe1e22e2932e4b7`  
		Last Modified: Tue, 09 Sep 2025 09:37:13 GMT  
		Size: 14.3 KB (14285 bytes)  
		MIME: application/vnd.in-toto+json

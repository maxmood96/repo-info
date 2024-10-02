## `clojure:temurin-11-bullseye`

```console
$ docker pull clojure@sha256:e0d33f36b73578db0c834c9738d4d06b16420a7a142eaf174208fa3073f3f107
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:33a4f4ec269c0e4657d5ef4be2b59f640e374fa9921bca1c63af9c9810fe186a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.0 MB (269966118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ceabd94365d373b5fb35a181c8c4a92cffeb5e769c4d2e4366cf659cc0593ae`
-	Default Command: `["clj"]`

```dockerfile
# Fri, 06 Sep 2024 16:59:26 GMT
ADD file:52a4b3d3a7281812594cb25cd6c6e83649d63a981e9f92f7c189ebe080249490 in / 
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
	-	`sha256:014ac6453c34f79cc163f6567c184e5eb0b48cdc07ecbfb1388d90e95ac90b02`  
		Last Modified: Fri, 27 Sep 2024 04:33:28 GMT  
		Size: 55.1 MB (55081391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d4aebe6aa495a52f6410fec3417c73614d4437cad01e2bf88756def8d3ce98a`  
		Last Modified: Fri, 27 Sep 2024 06:01:10 GMT  
		Size: 145.6 MB (145550047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a42ba101bf780440f72997e4fb20706a73ea584c646d8277d77751465a5c936`  
		Last Modified: Fri, 27 Sep 2024 06:01:10 GMT  
		Size: 69.3 MB (69334037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4b4681c9d811d3557009f1edfa351673250576451cbf65f8024436f24281084`  
		Last Modified: Fri, 27 Sep 2024 06:01:07 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:e9adf1bf25583774e7570d871fe36b21d4c63da717d14e2da6f58bf74171af21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7223999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1c3d6379ed975e8617be0a85271931b3d80dd6ad189c3d3be0aa108c6a95158`

```dockerfile
```

-	Layers:
	-	`sha256:fce41aa242cb2c86e98bd78e17c8b468ec13bd7f801f72de6b7e4a1217b48a77`  
		Last Modified: Fri, 27 Sep 2024 06:01:10 GMT  
		Size: 7.2 MB (7210134 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4a0c7388ca95ba99420ac39f2a79ef27568360cc9157922f3363dd453a9b425`  
		Last Modified: Fri, 27 Sep 2024 06:01:09 GMT  
		Size: 13.9 KB (13865 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:40cf6ee445aec8132e4f1b2f78d696122ffe3ab9e2c3fa15c0d75ad71107bd05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.6 MB (265556088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2da77328e9c507818b6634825954a66b75b1f325e140056f5ab57162b3c3d66`
-	Default Command: `["clj"]`

```dockerfile
# Fri, 06 Sep 2024 16:59:26 GMT
ADD file:20638e93d5a3e884b24b90ba3bef17ad5a4c795085c457bd5729f2f5caaf6a73 in / 
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
	-	`sha256:374a548aba539daa8d37f8b0fe7326b582daa60fe22cc343a838af2e82a4ca1c`  
		Last Modified: Fri, 27 Sep 2024 04:41:08 GMT  
		Size: 53.7 MB (53733864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6afe340dfe34e1f3b4368f84d8d80af89d978ff58a7685cc51fd2f1a89b4bc8`  
		Last Modified: Wed, 02 Oct 2024 02:11:38 GMT  
		Size: 142.4 MB (142354809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:292d218723fd45793ce7686c252f971ae6fb16bdf446d0a7fdd18e29307cbf03`  
		Last Modified: Wed, 02 Oct 2024 02:16:00 GMT  
		Size: 69.5 MB (69466770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:045d9fea2501cfd1af4b1ee7744bddccc24648eeea6c49ba3dd3756d4378a6c3`  
		Last Modified: Wed, 02 Oct 2024 02:15:58 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:636e1d8afe3aa05e9358e39580df7696f350db74e7d2a2545d2870b6f8875286
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7229868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35172f7a5a43e513dfb480905a83070ada6548afc24e7980a34fc7589e3f80e3`

```dockerfile
```

-	Layers:
	-	`sha256:86b0898b907a465b528e26fed2aa6e10b891d196b22a9d00b46db97b67487124`  
		Last Modified: Wed, 02 Oct 2024 02:15:58 GMT  
		Size: 7.2 MB (7215892 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6c0feca2e1377c3d265b2af8ea4dbd771bc728b12f94683a26b624dc36405fd`  
		Last Modified: Wed, 02 Oct 2024 02:15:58 GMT  
		Size: 14.0 KB (13976 bytes)  
		MIME: application/vnd.in-toto+json

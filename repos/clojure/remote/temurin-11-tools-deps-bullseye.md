## `clojure:temurin-11-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:d57a574abe7338c1f1b1af355456727204364b2fe99cfd590da7995886afb500
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-bullseye` - linux; amd64

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

### `clojure:temurin-11-tools-deps-bullseye` - unknown; unknown

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

### `clojure:temurin-11-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:9598f9817dd4708b505f90dbae87677e7a244efb38f289f00c42b472410469a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.6 MB (265553846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cfcf058b493a67d79a45fcd26d23ea3d2ff0b4a741a744112151afecc989719`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 04 Sep 2024 21:39:59 GMT
ADD file:aad8b86b3a958bc07504985acedcc819faa4f1ed12ca8b46d8d94c4d564cbdfa in / 
# Wed, 04 Sep 2024 21:40:00 GMT
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
	-	`sha256:d82c4492ee91810a42e0c53e955a661e9a092364bc474c9db559ea5b24b7047f`  
		Last Modified: Wed, 04 Sep 2024 21:42:52 GMT  
		Size: 53.7 MB (53731619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a366681dbb19e5f549205706d4f93f9a42c97048359666239e208d16c90d680f`  
		Last Modified: Tue, 17 Sep 2024 04:20:29 GMT  
		Size: 142.4 MB (142354815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:885d44361c8ede987d144a84e71eddb66a0b694987fea7346e84ce592e40de7b`  
		Last Modified: Tue, 17 Sep 2024 04:26:42 GMT  
		Size: 69.5 MB (69466764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13c96f83f5e9a299818310d02ac85ee778f018b8506373455b578a2972416116`  
		Last Modified: Tue, 17 Sep 2024 04:26:40 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:02f712f72421bf8c71fe442550d35582ea9b4b4d9825e7e86cc26e513d582e9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7060467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e0aace732584f3ba43b22f49af0fa8418148a2001815d949f0ec4bfd52a44f3`

```dockerfile
```

-	Layers:
	-	`sha256:ad76a4ac8e1ed0613e9a6f5a18da11f3b761a96d2b44b0f6a85c15751f712693`  
		Last Modified: Tue, 17 Sep 2024 04:26:41 GMT  
		Size: 7.0 MB (7046066 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f67cfa7289204dd90d616a5bdb998a88be8d7570427bb58b4bde67a5a36da87c`  
		Last Modified: Tue, 17 Sep 2024 04:26:40 GMT  
		Size: 14.4 KB (14401 bytes)  
		MIME: application/vnd.in-toto+json

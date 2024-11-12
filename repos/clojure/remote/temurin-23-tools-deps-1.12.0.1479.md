## `clojure:temurin-23-tools-deps-1.12.0.1479`

```console
$ docker pull clojure@sha256:2d99fa0b23c79f7d825a4f33a30e27b90e023e64180c546896f033fd9cf4acbc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-23-tools-deps-1.12.0.1479` - linux; amd64

```console
$ docker pull clojure@sha256:c9021a801d8205197e102ccb4af648fb718812ea22d10fe47bc2ebf3351896d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.8 MB (295810229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a2b11dff752dc0e929594a0146bda0b392cace75bb8404ed49076a77c2a2ea7`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b2b31b28ee3c96e96195c754f8679f690db4b18e475682d716122016ef056f39`  
		Last Modified: Tue, 12 Nov 2024 00:55:23 GMT  
		Size: 49.6 MB (49575695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b1d21051c4640be8d92999d473d97f5b00c12b3772eec17dd5b9709bed43750`  
		Last Modified: Tue, 12 Nov 2024 02:50:22 GMT  
		Size: 165.3 MB (165295128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cc5c24209ae10874a53d6679d1df47ac7f05009047792d5bf5ab31c71bed003`  
		Last Modified: Tue, 12 Nov 2024 02:50:21 GMT  
		Size: 80.9 MB (80938369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:516ece4db3e9a7b9b854c8fe865802d346e37c9a98e4a7e2f45e2593d60bd1a3`  
		Last Modified: Tue, 12 Nov 2024 02:50:17 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf37d98cf0921a429a673d782dcabca6f1fba146631b34c63f587b44f7f3d94e`  
		Last Modified: Tue, 12 Nov 2024 02:50:17 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-tools-deps-1.12.0.1479` - unknown; unknown

```console
$ docker pull clojure@sha256:d1cceb74c70634828f2bbbcef00e76d8e31aed8f402cbdb7303cbc66e33d205e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7204624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6335c150dbea9919cfc237f3126da7971f67bb0081ed88ded164dc2761bdcb0`

```dockerfile
```

-	Layers:
	-	`sha256:d8891de5e254e54fd3e142b53c9c636e625c72582b75088e9c9d407e6b53cdd1`  
		Last Modified: Tue, 12 Nov 2024 02:50:18 GMT  
		Size: 7.2 MB (7188120 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b704b4f6b57ae262e32069fa6f26fad3e81779844821bc92dc4b303c7e77723c`  
		Last Modified: Tue, 12 Nov 2024 02:50:17 GMT  
		Size: 16.5 KB (16504 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-23-tools-deps-1.12.0.1479` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:f0490dc0774fa0ca343a70cd1d33cf83b7ad704505219d3210d79c9e85cb02cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.7 MB (293658069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be6361a2e49d82caab39d91d2ba4e5b486cc69dcffb9b5ac22966ab12e876970`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD file:1df819221542e236e104deb2624ffe4efd79382aed25b3ab20088becaeadad31 in / 
# Thu, 03 Oct 2024 17:49:34 GMT
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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c1e0ef7b956a07c7b090256aa16cbb0550a34d0625d1d23c5b1a76e92a58d01e`  
		Last Modified: Thu, 17 Oct 2024 01:14:19 GMT  
		Size: 49.6 MB (49584978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03ae4b4414c973b15696a4b086371a7a1cf69de00c5e246ce7e063afef75db09`  
		Last Modified: Thu, 24 Oct 2024 09:36:08 GMT  
		Size: 163.3 MB (163281780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2108f867edf5fd315a94fa0d17e634fc826f07f1806fca24dcd8cc323be08c1`  
		Last Modified: Thu, 24 Oct 2024 09:42:22 GMT  
		Size: 80.8 MB (80790272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab7ee3ad95ea250aab1b1a9576c6cde686e9ae9020a953fc66136d16f87eb018`  
		Last Modified: Thu, 24 Oct 2024 09:42:20 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdea1357f979fc4b07a7b7f21df03ae77d94447a83e4b2f8e919deb5fc860ca7`  
		Last Modified: Thu, 24 Oct 2024 09:42:20 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-tools-deps-1.12.0.1479` - unknown; unknown

```console
$ docker pull clojure@sha256:3d7e564e8e19c9a151f0b3a9d257581b3cfc0c99db82f99d25ec3918fb86a723
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7209718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9741232fc17e861d6a3bf20b22f02611607042fd972dd40114aefe814f72bd0c`

```dockerfile
```

-	Layers:
	-	`sha256:1cd60f39f9a89971ef2a3e5c4d65e474b96588a663bd70581f86b2d2a2262823`  
		Last Modified: Thu, 24 Oct 2024 09:42:20 GMT  
		Size: 7.2 MB (7193254 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8bd17f17244017ba623241016a4b39e47d5e868af199a4f5d6bb792a5dc84aa7`  
		Last Modified: Thu, 24 Oct 2024 09:42:20 GMT  
		Size: 16.5 KB (16464 bytes)  
		MIME: application/vnd.in-toto+json

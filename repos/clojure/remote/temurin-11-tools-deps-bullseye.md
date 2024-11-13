## `clojure:temurin-11-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:8e00cc1822456bfd61a69f5429f2c8bb7053d50219fd987502173c474120f907
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:5a14e8b618c2df2bf5817abc8822aa3b077d5c67dfb92baecf4f49041afc8fc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.8 MB (269849539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b98b94c58c7ca28a3a5422fa9b86d2250b909537fd074c414bb8681ca2eefc03`
-	Default Command: `["clj"]`

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
CMD ["clj"]
```

-	Layers:
	-	`sha256:c2056d933cd629f55ac55802dda223f122286bf60ec42a24f0d0f6ae2615315c`  
		Last Modified: Tue, 12 Nov 2024 00:55:16 GMT  
		Size: 55.1 MB (55108780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98a7fa6ef21f8c4f3a082b2827afff734a0ee00170797a9f1656a165b5ff2b33`  
		Last Modified: Tue, 12 Nov 2024 02:23:58 GMT  
		Size: 145.6 MB (145601327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2431bf91610d18dd487e41f9d92a36f6f8c03bbb49c92e1f3ed2f5c07c4e25f4`  
		Last Modified: Tue, 12 Nov 2024 02:23:56 GMT  
		Size: 69.1 MB (69138788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d63e1d3aebb15a5d96d9ba49e3c474036bf5481dbd64a2493fda0485ccbc197c`  
		Last Modified: Tue, 12 Nov 2024 02:23:54 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:3d0880212af877b53daca0406e2472b6a82908957d0d156959a291d85d179702
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7250293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e68b59d124ec2e627ed3c05436de04f4ac562844bf03860dd4be0306575734ab`

```dockerfile
```

-	Layers:
	-	`sha256:ba3a6795c77536bab77779372199236a74e6c5613feed57429d4c6d126df198d`  
		Last Modified: Tue, 12 Nov 2024 02:23:54 GMT  
		Size: 7.2 MB (7236041 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50303bbad4c4d706f847a47b7494e2e674ba732aa9ac6e8439d6049dc7331381`  
		Last Modified: Tue, 12 Nov 2024 02:23:54 GMT  
		Size: 14.3 KB (14252 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:85835ff591bafa5d2537f20439e15ed03aee0464335aa59fb71532f1020efe70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.4 MB (265424792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bed55629d6cba04a1418fc04a6d1803e818b053059911f045dd0ef7f8f632cbf`
-	Default Command: `["clj"]`

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
CMD ["clj"]
```

-	Layers:
	-	`sha256:a839664fe62f615da74af799f94ccbc890a15d0f78470aac54302c2fd5475615`  
		Last Modified: Tue, 12 Nov 2024 00:57:41 GMT  
		Size: 53.8 MB (53757072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e75643a1f9307cf54d0088a5df18d761fa6204029dd968c2ebe3e5be4f2f04c`  
		Last Modified: Wed, 13 Nov 2024 01:11:38 GMT  
		Size: 142.4 MB (142389107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94cc2597ac3b2aae6f4639200cebe5fe838d65dbcd5918e2be2e52121621a9bc`  
		Last Modified: Wed, 13 Nov 2024 01:15:21 GMT  
		Size: 69.3 MB (69277967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a2bcfd9cbb2db618f4ef4a69b6e62b90dac48401f7dbba7f06bca1a37197dc4`  
		Last Modified: Wed, 13 Nov 2024 01:15:18 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:871945e50c8e918a502e609c6bed892450894bfec25ac300dbba606405ad5c90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7256133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aafe31b43cb595afbe197eb719aeb37487fd089ac989aced6b72ad3e295e38cd`

```dockerfile
```

-	Layers:
	-	`sha256:5749806b3c16c6f4b27df58af4950d11352fee0cea8359b53f677ff40ff18566`  
		Last Modified: Wed, 13 Nov 2024 01:15:19 GMT  
		Size: 7.2 MB (7241763 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27df3d7695ab2115b4b264139b8a4188432b65e80a36c1e61678cacf22041c6b`  
		Last Modified: Wed, 13 Nov 2024 01:15:18 GMT  
		Size: 14.4 KB (14370 bytes)  
		MIME: application/vnd.in-toto+json

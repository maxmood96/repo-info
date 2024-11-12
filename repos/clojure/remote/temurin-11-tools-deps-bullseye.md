## `clojure:temurin-11-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:5d9d09fbf71f63c0909e2cd6c971dd22dba776d1e2c1cd2fac0d23678930f7fe
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
$ docker pull clojure@sha256:f2a1429124223539ac38109c89d5ca0559c233f4baf8a661556fa86bda5072ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.9 MB (267896345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac60a210a74f8edf38409aabe1685848a07eb752f46543927870f274c3622c48`
-	Default Command: `["clj"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD file:bfb52ce9788d517977c9e84dad795a6adb46efc0e8eff88853137b783826c104 in / 
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
	-	`sha256:76475c2689e229fac9e8ba4a02e64decb7fd62b2a3e4ad65ba97f8e1a35471f2`  
		Last Modified: Thu, 17 Oct 2024 01:14:55 GMT  
		Size: 53.7 MB (53734895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dc87e9fd068f3bebd9583290a1e1d314efdb382e2f35ea1b89944dc152a3164`  
		Last Modified: Thu, 24 Oct 2024 09:05:19 GMT  
		Size: 142.4 MB (142389121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:881d5f46e725c5d03c937c30db20dd0534405068bb5ba766ca3658fb821424d5`  
		Last Modified: Thu, 24 Oct 2024 09:10:38 GMT  
		Size: 71.8 MB (71771687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1454a0f71ff9bca74c3993bbf0c4389515c5d2a31d43dc1ad81f178e70462230`  
		Last Modified: Thu, 24 Oct 2024 09:10:36 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:5e47bb314a4ae7a05beed3bd1f1969f302bd8558b9892017396e9bd55231cd65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7255909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffb33fcef3f81c500a63bea67d9ac4028a4cbdb458d8a66fd3183ef8af1c2243`

```dockerfile
```

-	Layers:
	-	`sha256:a5b46e87cf166a1f36d1785035207e582638a56fbdd1ac6e046d1238a2f885f7`  
		Last Modified: Thu, 24 Oct 2024 09:10:36 GMT  
		Size: 7.2 MB (7241727 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3312df5e909a56ffb38dee616cd568ee6fe5226425f357109eba9f28bb3349c`  
		Last Modified: Thu, 24 Oct 2024 09:10:35 GMT  
		Size: 14.2 KB (14182 bytes)  
		MIME: application/vnd.in-toto+json

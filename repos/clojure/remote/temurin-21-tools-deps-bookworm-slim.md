## `clojure:temurin-21-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:075ce2e36f0891f255c1699c43babf4b3f4e8dd22cd771465e0e15c832028c95
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:e4062db96cfb0b5a4c87ab43d3d1aa3132a194ca4b620d6b6fb6112e638c8c84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.2 MB (256178698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70d92c03451bf9934c49f096c4c5246b604ccad3f3ff14b15257be3be9c55dc4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD file:90b9dd8f12120e8b2cd3ece45fcbe8af67e40565e2032a40f64bd921c43e2ce7 in / 
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
	-	`sha256:a480a496ba95a197d587aa1d9e0f545ca7dbd40495a4715342228db62b67c4ba`  
		Last Modified: Thu, 17 Oct 2024 00:23:58 GMT  
		Size: 29.1 MB (29126289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2df8f519d0965fffacf4c8abd345fe7b9f455209c4cefc08803c6bdc1f2ce767`  
		Last Modified: Thu, 24 Oct 2024 02:56:06 GMT  
		Size: 157.6 MB (157568685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efa091620b0858e13ac536a46d37eb63b662122250efa94418abd9abcb421b37`  
		Last Modified: Thu, 24 Oct 2024 02:56:03 GMT  
		Size: 69.5 MB (69482684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a056e3481b0da1b2a9bf374360f225ccb5f90308e083c529d2f9ed9a41788ae0`  
		Last Modified: Thu, 24 Oct 2024 02:56:01 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e15fef7d5e9769f9704bd5385c0c14d431aa8cbef8b9ab3b3ba5b9caee56ecb5`  
		Last Modified: Thu, 24 Oct 2024 02:56:01 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:448fb932e08a47bdc85dd094b299538c740c3ea724f59ca41829f93c6ed468ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4940774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b16135d0347f901b25bc80fac6bfab09508b0083e3c48d180a97f94edb592003`

```dockerfile
```

-	Layers:
	-	`sha256:06da7aab4b33c22c53daa376eddcd4fe544e0b3ebda277e49522f1eb90943132`  
		Last Modified: Thu, 24 Oct 2024 02:56:02 GMT  
		Size: 4.9 MB (4924395 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3668748543cd222b32d63ab8fca80e0410f6cca847c35c3a31f1beed97a29297`  
		Last Modified: Thu, 24 Oct 2024 02:56:01 GMT  
		Size: 16.4 KB (16379 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:de29140e296fb22c8598f5699f7cc08e2e378df6663ba06e332492ac6270b13b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.2 MB (255248907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:704efd9fc292d1203235315705a116c0396a386c20137a863554fc8f6796bea2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD file:702193928cded0bcec5edbf4a5660961e7caef8c9d9cafea3337b7f6720c4464 in / 
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
	-	`sha256:83d624c4be2db5b81ae220b6b10cbc9a559d5800fd32556f4020727098f71ed0`  
		Last Modified: Thu, 17 Oct 2024 01:14:39 GMT  
		Size: 29.2 MB (29156341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c16ef64a611abb0917203f086cab4426e687c1c31700d511fdb759b51538f86`  
		Last Modified: Thu, 17 Oct 2024 08:20:06 GMT  
		Size: 156.7 MB (156746200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:159627b69b998cff9585a6578c6067800a37c62467796aceb2c93e4f518a0097`  
		Last Modified: Thu, 17 Oct 2024 08:23:55 GMT  
		Size: 69.3 MB (69345327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3fae276bf5794fefeb7d7f49a1839cbd5f077eb84d9b6ca9af597f80b869817`  
		Last Modified: Thu, 17 Oct 2024 08:23:53 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d77b2634f2cf8fb6b84e98b2d36a94696d19fd4bd8be8732895d5443c13e3fb`  
		Last Modified: Thu, 17 Oct 2024 08:23:53 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d01be75a580cdb5d3ff501fa9684c417bb50621ed94c13dc60b3b2f75cf79f4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4946734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:500a241f472807b67bea9ca6e9447fbe37ad9613ab2efcc28bc7d9a70d34b75a`

```dockerfile
```

-	Layers:
	-	`sha256:422cf4d49bf8072027de4f73132d4b041bfc0070c7ae95a0d600cb90ab82a3e6`  
		Last Modified: Sat, 19 Oct 2024 12:15:49 GMT  
		Size: 4.9 MB (4930183 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee54a5fec494a02c625bdec9aa576503b2d64eb7af32ab829e0287ad9d0fc54f`  
		Last Modified: Sat, 19 Oct 2024 12:15:48 GMT  
		Size: 16.6 KB (16551 bytes)  
		MIME: application/vnd.in-toto+json

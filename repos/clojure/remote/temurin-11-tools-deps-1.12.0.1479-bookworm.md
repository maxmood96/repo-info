## `clojure:temurin-11-tools-deps-1.12.0.1479-bookworm`

```console
$ docker pull clojure@sha256:9f0eaaa31f27665d2acf0fba5c4af974ce39dd1b5e66449e34808e96d16dc7d9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-1.12.0.1479-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:3d6c6f7fdbc540ae434007fa752faab48ebd1e45c2ebc22a68fd19a930767c65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.1 MB (276116205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75416d35bca7405a9b0c102b42f3dec5887386ad1ac77bf8dc8d935f0029df2b`
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
	-	`sha256:b2b31b28ee3c96e96195c754f8679f690db4b18e475682d716122016ef056f39`  
		Last Modified: Tue, 12 Nov 2024 00:55:23 GMT  
		Size: 49.6 MB (49575695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbc02d519527eb8c9b3469f3b1cb404ea5c0094d7355c8fd73c96f3f870bbb4e`  
		Last Modified: Tue, 12 Nov 2024 02:23:42 GMT  
		Size: 145.6 MB (145601329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0c2e85ef2b50ff2c5794c2ce789ad2748ac51e60024e853cf301c176056cf9f`  
		Last Modified: Tue, 12 Nov 2024 02:23:43 GMT  
		Size: 80.9 MB (80938537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a89299a58597e1de3a84b9d5c84d6a10bfde8d05a6ee7c637f21e45218cc556e`  
		Last Modified: Tue, 12 Nov 2024 02:23:40 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.0.1479-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:f6592025c9f1a89208dc193fc5b3eca489e698dc4ca3c8583bef98885c0ef93d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7216844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5aa01102bc1de04acdbce86f124bdc19fe433acee0f0386b00860f00729c9760`

```dockerfile
```

-	Layers:
	-	`sha256:96fd74c790d9b7f720fbcee928b85e28ea786d0b86dfd7fea0dc946c9802f44d`  
		Last Modified: Tue, 12 Nov 2024 02:23:40 GMT  
		Size: 7.2 MB (7202594 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d65d4c40f6c1981a2ede6d72b38ccf666594601b107020448032c681c9be5c8`  
		Last Modified: Tue, 12 Nov 2024 02:23:40 GMT  
		Size: 14.2 KB (14250 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.0.1479-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:6431fb364162d373c60e5fa9d1bbddd4478173955d0ae200cb6b4281e3ed2ac2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.8 MB (272775414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f20fcbcb07579ed8da997af81e077ef94d88b7112dc42512e57e02ce180a7c75`
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
	-	`sha256:1a3f1864ec54b1398987bbe673e93d8b09842ecd51e86ab87d64857b70d188b1`  
		Last Modified: Tue, 12 Nov 2024 00:56:20 GMT  
		Size: 49.6 MB (49587201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a344885a21a35bcebd1aa7ba847630155eb969fe4acf5f7acafe766865cf53bd`  
		Last Modified: Wed, 13 Nov 2024 01:09:26 GMT  
		Size: 142.4 MB (142389159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e548f246c9973c92c3a028855a76d8f13757395897a636259b2758d9a896ca8d`  
		Last Modified: Wed, 13 Nov 2024 01:13:28 GMT  
		Size: 80.8 MB (80798411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fda09c9b8f02646f6e5c9db83133ad3d69affe91dec1c84fa6867d98a4bea13f`  
		Last Modified: Wed, 13 Nov 2024 01:13:25 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.0.1479-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:e3ce30937776294fac97b6e99a51be8488e05520481c8944bbd441b49359d701
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7223351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8bf3063147150589f70f7bc81a6f4076f0b9d0e7d33a6928abcc4d192e3dc8a`

```dockerfile
```

-	Layers:
	-	`sha256:fc98623ddf61344c676762a39ffa39e154b5043e3a96a0a43a7783b137dadc4c`  
		Last Modified: Wed, 13 Nov 2024 01:13:25 GMT  
		Size: 7.2 MB (7208981 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:416ef9863cc911f2c482580af8eb490cb6af5608ad066ba2da06bfd4da37ca9e`  
		Last Modified: Wed, 13 Nov 2024 01:13:25 GMT  
		Size: 14.4 KB (14370 bytes)  
		MIME: application/vnd.in-toto+json

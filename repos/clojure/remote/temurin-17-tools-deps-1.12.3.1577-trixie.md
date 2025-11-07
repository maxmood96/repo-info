## `clojure:temurin-17-tools-deps-1.12.3.1577-trixie`

```console
$ docker pull clojure@sha256:99e0ec635dcff8094e4542964889886af4c51e8fcb43749a29eb24dfdc2006df
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-1.12.3.1577-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:055af9d4a8106210061856592158b92e8f19a0cba90713be70afb1f2ad3a988c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.5 MB (279520389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f58bac0c418f4118e56103468f6eff04de98667491e76b8a4ff3278631c3e5c3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 04:30:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Nov 2025 04:30:49 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 04 Nov 2025 04:30:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 04:30:49 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 04 Nov 2025 04:30:49 GMT
WORKDIR /tmp
# Tue, 04 Nov 2025 04:31:05 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 04 Nov 2025 04:31:05 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 04 Nov 2025 04:31:05 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 04 Nov 2025 04:31:05 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 04 Nov 2025 04:31:05 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:13cc39f8244ac66bf1dd9149e1da421ab1bbc80d612dc14fe368753e7be17b33`  
		Last Modified: Tue, 04 Nov 2025 00:13:22 GMT  
		Size: 49.3 MB (49285628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d8f6ceb625bf35f4777143cee4edabf9ac01b3d7ec4900e16dd285aff2e73df`  
		Last Modified: Tue, 04 Nov 2025 12:10:50 GMT  
		Size: 144.7 MB (144693293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44fce969fb0918f8f3db889a1476dafcee58551fe19cb3ad0b3ae051a66576ea`  
		Last Modified: Tue, 04 Nov 2025 04:31:38 GMT  
		Size: 85.5 MB (85540425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6a0df655aa3ca309f55145ae8bf6f3908eb88fa0e26aab832b04a3a944bc903`  
		Last Modified: Tue, 04 Nov 2025 04:31:31 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0794a84a78a94a1b9bb9797f562dc5cdf521619a001d4c61c6b4b4af5a3fc830`  
		Last Modified: Tue, 04 Nov 2025 04:31:32 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.3.1577-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:0489f05a9aed06043b8381ced8b44206c6b8ac610b72b2c6aa4780be96a49c01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7482653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbbb63cc8c4763f709e7fc770287ddebbdbdb08d99d4b29246415f6e32897f6f`

```dockerfile
```

-	Layers:
	-	`sha256:898d1710dbb63d7986140556ce8bd9000f4f484dd8b2bf18393840e2ec13d968`  
		Last Modified: Tue, 04 Nov 2025 10:41:21 GMT  
		Size: 7.5 MB (7466899 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8975e19b6686f4d263d09d067d52a1f5f1eb64c6f040f7b416a2343802daeb8d`  
		Last Modified: Tue, 04 Nov 2025 10:41:21 GMT  
		Size: 15.8 KB (15754 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.3.1577-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:e82f210bed4a4e43f6e4d0cf69a88854fc54a299236f5acc777f1690fefec4fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.6 MB (278556817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f02535b2401b4df8859a7ccbeb71f88251530282a1999c80d11833a160cb84c0`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:44:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Nov 2025 01:44:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 04 Nov 2025 01:44:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 01:44:36 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 04 Nov 2025 01:44:36 GMT
WORKDIR /tmp
# Tue, 04 Nov 2025 01:44:54 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 04 Nov 2025 01:44:55 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 04 Nov 2025 01:44:55 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 04 Nov 2025 01:44:55 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 04 Nov 2025 01:44:55 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:04077a68e2b807cad70ec4dfc0a2e8e1ff1ea6d9523e4c8f042b9a1ae8a54409`  
		Last Modified: Tue, 04 Nov 2025 00:13:46 GMT  
		Size: 49.7 MB (49650430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b2fd3ab44fa4c5773b2dfaa01c142bfda274f38afc1530e315e1245cb1dbb55`  
		Last Modified: Wed, 05 Nov 2025 13:22:16 GMT  
		Size: 143.5 MB (143542106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a4c7af8f60ac95352b8ee207567327b6cf3e37d5365232ff3ea3fd573e4df16`  
		Last Modified: Tue, 04 Nov 2025 01:45:40 GMT  
		Size: 85.4 MB (85363240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9af6fe7fbd510b122afdecc4598ab8802e2866efbd19b16f64e57695347bc9f6`  
		Last Modified: Tue, 04 Nov 2025 01:45:28 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:390f11b17fc0c39ef59002a1e125a145606a893b1b6884e37936367869c35d13`  
		Last Modified: Tue, 04 Nov 2025 01:45:28 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.3.1577-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:1b05c0c9da28a628c4c515fd58c23c029df70383471c496a1390a6dbe02e490d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7489801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8afd72951febf4536e373065c523f5ca2d78a44a63e8a8a303d983811bf3fc3b`

```dockerfile
```

-	Layers:
	-	`sha256:22413f2b92bfae41c42e62e15ffef461e7c8b3723a5a3170d2876e35aefc7261`  
		Last Modified: Tue, 04 Nov 2025 10:41:27 GMT  
		Size: 7.5 MB (7473929 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a575ef4b3149f524794896159ec3072f386b17fd42471928f585f67708b73376`  
		Last Modified: Tue, 04 Nov 2025 10:41:57 GMT  
		Size: 15.9 KB (15872 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.3.1577-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:1d93b27bf02d1e041e7b3fe2b72caad3c740b144ba339f116ab344da04914f2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.4 MB (288433940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:139f4a1b10d0751ff678bacf6e992dcbc6f92e5bc39ca087159148a49ef64339`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 13:24:19 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Nov 2025 13:24:19 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 04 Nov 2025 13:24:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 13:24:19 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 04 Nov 2025 13:24:19 GMT
WORKDIR /tmp
# Tue, 04 Nov 2025 13:30:43 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 04 Nov 2025 13:30:43 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 04 Nov 2025 13:30:44 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 04 Nov 2025 13:30:44 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 04 Nov 2025 13:30:44 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3c335bb15935da0eae5ce30111cfa6a289c813162bada9fd389d8ae5510d5d66`  
		Last Modified: Tue, 04 Nov 2025 00:20:22 GMT  
		Size: 53.1 MB (53110127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbb09d1935d5dcfb59c2b828f8730e2e0cc1200d9a83398904ff45bff51cda4b`  
		Last Modified: Tue, 04 Nov 2025 22:42:40 GMT  
		Size: 144.4 MB (144372909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f22d2a12245b67c14c93b30d6df8b0c97f0c5b6ae82218c8c850b4fb70d9edc2`  
		Last Modified: Tue, 04 Nov 2025 13:31:42 GMT  
		Size: 90.9 MB (90949858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a5936e3fbe9635002e8f2787c4846fa3fb95de70ce96c1635b158d0b605dccd`  
		Last Modified: Tue, 04 Nov 2025 13:31:35 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e20a4db4dcd7037cc73707f2d81a9dced949ed598b88a1eccab519a50046946`  
		Last Modified: Tue, 04 Nov 2025 13:31:35 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.3.1577-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:55d4f5014b1698e3fee4cadab00a8f7f602c85d5037be4c63bd035dacd7ab811
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7486319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b67dd6e8fe732b61a838e6c1ddfc4a9b7d471fe684f3e756051ea6049e07a2b8`

```dockerfile
```

-	Layers:
	-	`sha256:bf9594b7594ead2da1b066c4e717c3fb4cca7667202657c03db1d50d5db95821`  
		Last Modified: Tue, 04 Nov 2025 16:37:33 GMT  
		Size: 7.5 MB (7471318 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1469afbae60c819d789707846ed9b791ffc900975d123f8c687f5791909ef21`  
		Last Modified: Tue, 04 Nov 2025 16:37:34 GMT  
		Size: 15.0 KB (15001 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.3.1577-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:8da4e752e538dcd1843b015886c18dffc9393fd0fb7da7a19cecf8bfff238fe3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.8 MB (270774420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f746f5fd34fd983e5d2665c76836fceffce8cbfc9a9d7b6921b8d15c684008b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1762202650'
# Fri, 07 Nov 2025 06:05:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 07 Nov 2025 06:05:53 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 07 Nov 2025 06:05:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 07 Nov 2025 06:05:53 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 07 Nov 2025 06:05:54 GMT
WORKDIR /tmp
# Fri, 07 Nov 2025 06:21:13 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 07 Nov 2025 06:21:14 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 07 Nov 2025 06:21:14 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 07 Nov 2025 06:21:14 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 07 Nov 2025 06:21:14 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:de6b66e2abcf55248485e438d6def9b92cf28773b7cd7896ee78f9409b6e7526`  
		Last Modified: Tue, 04 Nov 2025 00:27:48 GMT  
		Size: 47.8 MB (47770924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0c954b8170eabf573a80b99d49dd9da69985111271e239b9f7af18ceb6ef66d`  
		Last Modified: Fri, 07 Nov 2025 06:11:48 GMT  
		Size: 138.6 MB (138575651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ff3d8d663fe408bff616f173ff117ba24748cc7bcd621a7fab20e94db0ebc03`  
		Last Modified: Fri, 07 Nov 2025 06:25:56 GMT  
		Size: 84.4 MB (84426805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ca15f0e196e06825485ea422a1008bdb174ce43f36d57b1d8c8de64f4c73e26`  
		Last Modified: Fri, 07 Nov 2025 06:25:49 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1f9b663afe0128ff105d16839d21e1860f81a810f3af0edfda147114974d2ee`  
		Last Modified: Fri, 07 Nov 2025 06:25:48 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.3.1577-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:0f871533fe1a60a275565f6d80b0168c311bf6677dc4af811258f47f9e0a185c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7468695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f04395a1da8bb6523583b2ab7ab84d12c536054c6d49032e7d04aea9a12fb0e`

```dockerfile
```

-	Layers:
	-	`sha256:6deb57c7051c612d52618dc94ef235e214e6aa1c2a5469818ec40379262470e0`  
		Last Modified: Fri, 07 Nov 2025 10:36:14 GMT  
		Size: 7.5 MB (7452893 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ddb9ff3fe9e9c5d90726c3e39a73a6afc2bff4dc201f40fd8fae324df195f97e`  
		Last Modified: Fri, 07 Nov 2025 10:36:15 GMT  
		Size: 15.8 KB (15802 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.3.1577-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:c812bcf5e5f1b61395371d4d6515ac78769b03c540c1d483c2ab1525a2166fe7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.6 MB (270585835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:921ff82ab1cd8f1c9b5c00015d9637a29ec6da111e086122d5df3a631ac6aa1a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 12:59:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Nov 2025 12:59:31 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 04 Nov 2025 12:59:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 12:59:31 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 04 Nov 2025 12:59:31 GMT
WORKDIR /tmp
# Tue, 04 Nov 2025 13:02:22 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 04 Nov 2025 13:02:22 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 04 Nov 2025 13:02:22 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 04 Nov 2025 13:02:22 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 04 Nov 2025 13:02:22 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:48bd359f940d437208e8579c571291503fa327e04a66a6c8d918cfe93cae2e1e`  
		Last Modified: Tue, 04 Nov 2025 00:19:45 GMT  
		Size: 49.4 MB (49352299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc8caae96ef3e33780620b5029c31906f23b6496c68aac3becdf6358b74de74a`  
		Last Modified: Tue, 04 Nov 2025 23:01:24 GMT  
		Size: 134.7 MB (134723624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10f7e1c8bdfe5d5a36abaf62491ea4290b9b1dfb6692685695d8889d02b3c3af`  
		Last Modified: Tue, 04 Nov 2025 13:03:13 GMT  
		Size: 86.5 MB (86508870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:939d682ffe5dc7c9a3d1f8343e227f0f8bdde7983877a856476e58cb302c28ff`  
		Last Modified: Tue, 04 Nov 2025 13:02:54 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36ebc2bf002d362f9b2cdb3efe9b5a1d6d0a263a8183146405432c6fc20d2cdc`  
		Last Modified: Tue, 04 Nov 2025 13:02:54 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.3.1577-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:ad2acae2c2d82daf9ecd280186c1f8e266268343252a4c4047a3e7c41a18fa70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7477774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7b46c0b66e53307d4b8d8afbf45893c65fc0dd44bbbb42da6d4de61d2afb7bb`

```dockerfile
```

-	Layers:
	-	`sha256:3f16923b3ad420252c852ef56878e7aaa127da1f95f54168aed00df875af4309`  
		Last Modified: Tue, 04 Nov 2025 13:36:31 GMT  
		Size: 7.5 MB (7462821 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b54c75f72e4be8f0e8fa39e83462713a769d0fa592f366d5b8c99355f3191c3`  
		Last Modified: Tue, 04 Nov 2025 13:36:32 GMT  
		Size: 15.0 KB (14953 bytes)  
		MIME: application/vnd.in-toto+json

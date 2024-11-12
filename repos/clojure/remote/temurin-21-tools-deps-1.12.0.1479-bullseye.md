## `clojure:temurin-21-tools-deps-1.12.0.1479-bullseye`

```console
$ docker pull clojure@sha256:7761acb2b9151c3fec11c1fba6aa7a8def141d023e080b464738a415810b57d9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-tools-deps-1.12.0.1479-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:5def7dc5d081209ee67e17142b65e27cbec401ebaaae6b31b9e616b592c6743c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.8 MB (281816979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98a2b13d2440e21621d50401f2f7a349307f467985a765730ca53270abc21dc3`
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
	-	`sha256:c2056d933cd629f55ac55802dda223f122286bf60ec42a24f0d0f6ae2615315c`  
		Last Modified: Tue, 12 Nov 2024 00:55:16 GMT  
		Size: 55.1 MB (55108780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5a20a48b0cec7d3bd3962ead3b379527c4cbe34db0cebb7872c357a9533e26a`  
		Last Modified: Tue, 12 Nov 2024 02:49:35 GMT  
		Size: 157.6 MB (157568719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12bb004160a868de854552856693edd439fd2f57b3245b5caf1742630519a69a`  
		Last Modified: Tue, 12 Nov 2024 02:49:34 GMT  
		Size: 69.1 MB (69138442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2722958bcbc5bc9bfe5ccda9cb5f86757a74ce0c0fac764b2b6cce3af30f19b`  
		Last Modified: Tue, 12 Nov 2024 02:49:33 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81d0676ed45cd48c1e4e09da26d4ef790c998fef5ffe3e688a0923635652f219`  
		Last Modified: Tue, 12 Nov 2024 02:49:33 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.0.1479-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:aa58b60106ebd56fe54f9b198605684128a11b6d5f945dfa59150cb45c4226ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7236150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e6e1cfb2f32148aafe405569498978308a563afe7c80642ca3e6ac4e3e1b601`

```dockerfile
```

-	Layers:
	-	`sha256:0c4c631e2f692f2801606bfd0ad95bf98388ccd8a4bf534903bd3ea103dd502f`  
		Last Modified: Tue, 12 Nov 2024 02:49:33 GMT  
		Size: 7.2 MB (7219653 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:175b54051b0f71d252996ea736a024a32798779e3af3a9f007d902c70510203b`  
		Last Modified: Tue, 12 Nov 2024 02:49:33 GMT  
		Size: 16.5 KB (16497 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.0.1479-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:1069e696d1c8ad246a285efa91bd771c054d0371e0bb22168c106d4511c72714
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.3 MB (281300656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2db7bffcd955e7dcf38e4649b81210477248a449ed79a78afc62525e54646d69`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:76475c2689e229fac9e8ba4a02e64decb7fd62b2a3e4ad65ba97f8e1a35471f2`  
		Last Modified: Thu, 17 Oct 2024 01:14:55 GMT  
		Size: 53.7 MB (53734895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dda1f5042875c6cd55ec9afb14d7d146178d30c5c91dbfde893cd3a021c8420`  
		Last Modified: Thu, 24 Oct 2024 09:26:33 GMT  
		Size: 155.8 MB (155793065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21796739361946ac45b4d37ee3b83266453c459ab57c41133f3d0a6610a1b014`  
		Last Modified: Thu, 24 Oct 2024 09:32:26 GMT  
		Size: 71.8 MB (71771658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b10ab76587a047c127759aaffbb428170f7d17b9862b2f7850a035fda705f76`  
		Last Modified: Thu, 24 Oct 2024 09:32:24 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83eb303a070a9037c6ce9b3380cb4884c6a00fe5c1f4e1e250785edd49cf5642`  
		Last Modified: Thu, 24 Oct 2024 09:32:24 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.0.1479-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:bbe29fc04e555f3a3808e5b92c0a08fa6ecdfb7acf3228989d713a080c8f1c97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7241202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0f61f4242e1ad71456a9398caad7a746d18d908927574206a162d982764ebd7`

```dockerfile
```

-	Layers:
	-	`sha256:1114014b40989bcbb7b58685c5613a6f9ffe4ce641213e73b269dd59be4d3446`  
		Last Modified: Thu, 24 Oct 2024 09:32:24 GMT  
		Size: 7.2 MB (7224744 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:751c80c4c0de3279d2ea01a8527d0860bac8a7b39589b58004a6a8283a2ea324`  
		Last Modified: Thu, 24 Oct 2024 09:32:24 GMT  
		Size: 16.5 KB (16458 bytes)  
		MIME: application/vnd.in-toto+json

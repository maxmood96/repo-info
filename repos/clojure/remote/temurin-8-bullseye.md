## `clojure:temurin-8-bullseye`

```console
$ docker pull clojure@sha256:20338a02905301ca6fdc59014af19002fdcad20dfedc1a55a922a3e362acf0f8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:e3aece68cc737dbf2a90857cf695eaecaac14a9abe8a4b4c37e2292df310673c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.0 MB (178044190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:059eb1f825d07337a3dd9ddc308ba0c313a8e26f0c0cace1acf52492cce3aeac`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1754870400'
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
	-	`sha256:078965fc7cf303b72cc4eef5479dc2dbf5bc84fb8e6052a89b9b5362e14b3651`  
		Last Modified: Tue, 12 Aug 2025 20:44:43 GMT  
		Size: 53.8 MB (53755344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9d58103980be139b3e3768bb2cbf263c6178b4f88d27d8f24857bb806dc1f2f`  
		Last Modified: Tue, 26 Aug 2025 17:28:17 GMT  
		Size: 54.7 MB (54731349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6431142a0e2fdbd42350904eedac73241259656b26ed801be82a17eb38c5897c`  
		Last Modified: Tue, 26 Aug 2025 17:28:01 GMT  
		Size: 69.6 MB (69556851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68b1e4552dda6f261229f491d86781060c365a6608272420c688326102055ecf`  
		Last Modified: Tue, 26 Aug 2025 17:27:52 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:e279b9b34eb9301d645f0329b309ba1b25e9cb9f1ff61dc41459ee5e0f70bdfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7531514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4c5aef0231725b5e5cf22d920d9c60bc8454061e415868f8de55d09eaecc3ca`

```dockerfile
```

-	Layers:
	-	`sha256:59d42257f82c023b189185cce45cea2b97899b0b1e00c5939f94ab1deb22b7e4`  
		Last Modified: Tue, 26 Aug 2025 18:44:46 GMT  
		Size: 7.5 MB (7517277 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8bec02ff201967d042806dc9dcb24ebe9f8064f214959c99884a122be904caf`  
		Last Modified: Tue, 26 Aug 2025 18:44:47 GMT  
		Size: 14.2 KB (14237 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:5741339bfbb7ef5106db2ade49bf85d54114f69b6f55f5bec2df885625d80bef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.8 MB (175768602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9b2014474e5cc01462ef89f5c417262ea3772165d113a34d6f0f7c37bcbcb3f`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1754870400'
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
	-	`sha256:7b68ea47bc3cd8615e51fdbe0976cb4999ba56ce8764e755543a4521d69a32f6`  
		Last Modified: Tue, 12 Aug 2025 22:08:57 GMT  
		Size: 52.2 MB (52248409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3c68418c918156697c68aa13e1642c98a2beeadf9646a706b7123bd36165147`  
		Last Modified: Mon, 18 Aug 2025 16:54:18 GMT  
		Size: 53.8 MB (53835632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e2f5df1b7038925821c5a1bb27a61a3d582ae1d5d94168268c7def7897459a0`  
		Last Modified: Tue, 26 Aug 2025 17:29:30 GMT  
		Size: 69.7 MB (69683915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b7161d2fda7ab8aea5de6d2ca474e00ba9bac843f6583c2c649262df69f0197`  
		Last Modified: Tue, 26 Aug 2025 17:29:16 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:d18cfbc1fe7bc5ba5a95a6e0a1b3f3f551f8b0e79c3d3a68029e379931a5d2b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7537427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eae55ed06ccd3e905a6cf3c54692182f9ba200abf5732e884dcf01d085c2cef7`

```dockerfile
```

-	Layers:
	-	`sha256:4e3df5b26ad25295d75b14fe9e7ead34ad4eb4608c623b107e3e2955635f30c6`  
		Last Modified: Tue, 26 Aug 2025 18:44:54 GMT  
		Size: 7.5 MB (7523074 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a51e3854c86f98fa6a560aae17457795ee0eec531427dac3e73813081cbc806c`  
		Last Modified: Tue, 26 Aug 2025 18:44:55 GMT  
		Size: 14.4 KB (14353 bytes)  
		MIME: application/vnd.in-toto+json

## `clojure:temurin-17-bullseye-slim`

```console
$ docker pull clojure@sha256:14871fe4ce36bb73affe516574bae286ff5c30fe37e1468927e635cd89cc76f5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:1d4c38d169e3e50ab0b34388e5363002c2b69555a64e11030b3d6ae2802d882c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.6 MB (233571385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7c9cb7a939e8602433bbbe04ca066df0f3f786cfc458bd1ea9e8b6c826c20fc`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Jan 2025 23:07:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1736726400'
# Mon, 06 Jan 2025 23:07:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 06 Jan 2025 23:07:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Jan 2025 23:07:46 GMT
ENV CLOJURE_VERSION=1.12.0.1495
# Mon, 06 Jan 2025 23:07:46 GMT
WORKDIR /tmp
# Mon, 06 Jan 2025 23:07:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8408034c095c531155acb08bef65ad1edf25f55226bb086dfaf0d0eee9cadd59 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 06 Jan 2025 23:07:46 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:89320e7119e225692d79aaeb4989a18d7f97daafdb2b3782f84a0a8de31a09de`  
		Last Modified: Tue, 14 Jan 2025 01:33:29 GMT  
		Size: 30.3 MB (30252665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95dd7cc2363b1270d0cab04c478e9ac45dc963182891668e6427203b8ce4a982`  
		Last Modified: Tue, 14 Jan 2025 02:44:37 GMT  
		Size: 144.5 MB (144536708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44d637f6ffe9fdb1e261c3f4ced529e61c7458d03ef60693e4749e9f840c7404`  
		Last Modified: Tue, 14 Jan 2025 02:44:35 GMT  
		Size: 58.8 MB (58780973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:756b98186115768b8d510bf5d0d25b7974b99dc766d29a207cacb55d3effa16b`  
		Last Modified: Tue, 14 Jan 2025 02:44:34 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33fda6e07bc0a6501cfd6a941390d8c848e10e4528f24599d0721b6ad7fe2e21`  
		Last Modified: Tue, 14 Jan 2025 02:44:34 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:5b59d0eb502cf94089f050bb038f938bf90df37cbec60202a9f56278f0bab18a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5132948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2ed9fcaac02a75d2bae6dedf6c956ac9af66bc465ee5ab8fc8c9f487cb7374f`

```dockerfile
```

-	Layers:
	-	`sha256:43ff16a24ee925a0ae3c7a45282d328a5cc385adb5fd41234b5228c12b89fbfb`  
		Last Modified: Tue, 14 Jan 2025 02:44:34 GMT  
		Size: 5.1 MB (5117069 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b2d71ca1a4072f5f9b1a6e4b1778cf203ed2625efca10ed2ca0a06060c0be211`  
		Last Modified: Tue, 14 Jan 2025 02:44:34 GMT  
		Size: 15.9 KB (15879 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:2573a773fa777767f56205d7a811f40469c37f4a7a8f4da7d94434aef442db22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.0 MB (231012052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1524837ceff91d66d84564267803c935cb423feb212c6dae23b206ee2963470e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1734912000'
# Mon, 06 Jan 2025 23:07:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 06 Jan 2025 23:07:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Jan 2025 23:07:46 GMT
ENV CLOJURE_VERSION=1.12.0.1495
# Mon, 06 Jan 2025 23:07:46 GMT
WORKDIR /tmp
# Mon, 06 Jan 2025 23:07:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8408034c095c531155acb08bef65ad1edf25f55226bb086dfaf0d0eee9cadd59 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 06 Jan 2025 23:07:46 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:879a6187682fc52c69294a2f450abdb54e257a50e8133ec6e89cb140345be6ce`  
		Last Modified: Tue, 24 Dec 2024 21:34:50 GMT  
		Size: 28.7 MB (28744853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8bfdadce1216dd298f1b476897a36dc506dec08d9613ab2d5e49cd1a5534d6d`  
		Last Modified: Wed, 25 Dec 2024 02:14:36 GMT  
		Size: 143.4 MB (143361000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70cac89ab88899b85ee654dfd5e62e719d65d297526aedaebffd0817f57d8389`  
		Last Modified: Tue, 07 Jan 2025 03:29:10 GMT  
		Size: 58.9 MB (58905158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:186689c1428aa8e5ca923e43d323d18c8ff30835494e4c7d8100875ce930f692`  
		Last Modified: Tue, 07 Jan 2025 03:29:08 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f77c3507a5c77aac1588ad67e5b405cc30f08394b95d4597426b17ecc21fd0b`  
		Last Modified: Tue, 07 Jan 2025 03:29:08 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ac700b9d973fab798c801a0ebd4d08ceb3255cfed10423314bc97ad8a2f144ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5138797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99389b39b2dd0aa410093f47b5ac9a21505c641a9b768e37977f9b689938adcb`

```dockerfile
```

-	Layers:
	-	`sha256:2e36b57a163c4df450d5b121870f061af553fe1524c15a3b39a0f923178b64a7`  
		Last Modified: Tue, 07 Jan 2025 03:29:08 GMT  
		Size: 5.1 MB (5122801 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1b9fa0373ac8a5b4e5dd5695d437db5ca15445099836e7bf9bdc6e341aeb45e`  
		Last Modified: Tue, 07 Jan 2025 03:29:07 GMT  
		Size: 16.0 KB (15996 bytes)  
		MIME: application/vnd.in-toto+json

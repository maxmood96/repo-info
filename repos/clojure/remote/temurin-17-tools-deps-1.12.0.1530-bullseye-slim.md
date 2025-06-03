## `clojure:temurin-17-tools-deps-1.12.0.1530-bullseye-slim`

```console
$ docker pull clojure@sha256:19f5d1b2841b4023cd2faf78825dc4d37f31b9e76639cd0cd0569c3fe361bb3d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-1.12.0.1530-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:027865c65afd554ed1e0c1838ca4d289fbb0a4f92c34efafeab870f9b6536fcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.9 MB (233886144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbd51fdc782c073dc22a3a66f4f8020d2728ce4152fb3481b5d722bf123d1a02`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:e1f16b66c2e86ad38458eba597e4ec79e4750398a28dbbc2d7819d829c4c9023`  
		Last Modified: Tue, 03 Jun 2025 13:30:16 GMT  
		Size: 30.3 MB (30255940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2759b25f962276d5c941b87b4ee426d90184a15cd81228f42b8bb9c9495106e7`  
		Last Modified: Tue, 03 Jun 2025 13:50:12 GMT  
		Size: 144.6 MB (144634987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f31fa9120b614ec81d8c099f8ad0cd3c2e923197e987a397eff706db812aa07`  
		Last Modified: Tue, 03 Jun 2025 05:16:27 GMT  
		Size: 59.0 MB (58994176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:783ba34127d6d681835f335a93902a3488cac3acceb92b1c9753711eee009612`  
		Last Modified: Tue, 03 Jun 2025 13:49:55 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f24d847bdc7aef64af08b426edca36df78a651fcf820c9fbaff6e98ac2c68bdd`  
		Last Modified: Tue, 03 Jun 2025 13:49:54 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.0.1530-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:2aa062b1a35cbc9ec4813c0322a6449fbb920591fb06078f9e582669096338ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5184465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d17e6538b9e27fa5bd272add789ba0d84c72bffb9d5a056ae2e2b468a7df99ed`

```dockerfile
```

-	Layers:
	-	`sha256:d33d0db63e5e1f6f0be0c758ccac8eb60a1235172b499ce97118e149f98c4a3a`  
		Last Modified: Tue, 03 Jun 2025 05:16:26 GMT  
		Size: 5.2 MB (5168586 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b3da366c1b1af0567e735221c00cf14d1946b3dd708ac920316332657596108f`  
		Last Modified: Tue, 03 Jun 2025 05:16:25 GMT  
		Size: 15.9 KB (15879 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.0.1530-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:a29cacc65b363d77c12828e7bf41d5e8cec2e9f8743e3ad55b55157cf7c1379d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.4 MB (231388893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32593512a5af9366d9b21a8e40ff73b4973268118cb043da9620d0e5d305541a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:66850c8b65c1e9c3674a722b71f8887dd317a9b257148bb1063e88d85790544f`  
		Last Modified: Tue, 03 Jun 2025 13:30:45 GMT  
		Size: 28.7 MB (28746257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8312cdb9051efb69c102039d6eddfca07c90fb35536c0a89ddf1296555f86542`  
		Last Modified: Thu, 22 May 2025 03:15:08 GMT  
		Size: 143.5 MB (143512634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0349280929762625e2ab627884dcf475e83a6b8e9cb885ce0dbf83f86596f46f`  
		Last Modified: Thu, 22 May 2025 08:27:06 GMT  
		Size: 59.1 MB (59128962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c8791fecd373a236a98f4e8490efee8dc69d3e16c1d0fb6608811087fbd6855`  
		Last Modified: Thu, 22 May 2025 08:27:04 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0a6b19db3e3e69fe4144a4d3eb1a4c420e2371ae4e3c55ca1fb47f283edb1c0`  
		Last Modified: Thu, 22 May 2025 08:27:04 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.0.1530-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:bffd0f5ba9ece8aedc64cbc3c1e959e0cf87527f837a2668ad7475ba269e266d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5188719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:128863a6e9714c1d4b032f2f42553931c2cdfb810b47af8ccbea95abf6fc587b`

```dockerfile
```

-	Layers:
	-	`sha256:b7a60150e1c0e8fa54959205a9fa76897e00fd3048aa481def78217b28c6367d`  
		Last Modified: Thu, 22 May 2025 08:27:05 GMT  
		Size: 5.2 MB (5172722 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22b902a0817f113805d5d8150a862d788922fb38f5ff0a1a383fa8f4a8961bc8`  
		Last Modified: Thu, 22 May 2025 08:27:04 GMT  
		Size: 16.0 KB (15997 bytes)  
		MIME: application/vnd.in-toto+json

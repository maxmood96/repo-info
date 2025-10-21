## `clojure:temurin-25-tools-deps-1.12.3.1577-bullseye`

```console
$ docker pull clojure@sha256:9c5cbb49edb1762595e373ab567ee29f82366561892e5c9a5e3ef20ea8fdaf9f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-25-tools-deps-1.12.3.1577-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:5b2c1c880f0dc46d3263535336074fb48da8a03976545f27c63da6cd2e282c56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.4 MB (215352797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed4ac8a181c6f4c0516a01d404351e6ec3e3a11337f57cb0917749a5ef5a3a2b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1760918400'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b6f830cd306f01980373f1e0120f2d00018fbe51a9506b7262f5d9e4bbda74f9`  
		Last Modified: Tue, 21 Oct 2025 00:19:19 GMT  
		Size: 53.8 MB (53756115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c5357fbceade5055387906d1d209f6e3b77b6aa1efef526d9c00d640ea05318`  
		Last Modified: Tue, 21 Oct 2025 02:24:36 GMT  
		Size: 92.0 MB (92036044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fd17a36e3a9b2f90ea338212f6e5592d9a04d689d4124cec52bede881ece5f0`  
		Last Modified: Tue, 21 Oct 2025 02:24:37 GMT  
		Size: 69.6 MB (69559601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a1054482eff195feab1808ef5b57888a2787e46005c3ddcba6c9feee6106b7e`  
		Last Modified: Tue, 21 Oct 2025 02:24:31 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a7a208fe69c88a2ca06148fbffe21f9baffd75e594a33323be303e9a4e3e71b`  
		Last Modified: Tue, 21 Oct 2025 02:24:32 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.3.1577-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:b0fe7945368ff9badfc1fe1192e7894afb311f00d339ee1499f21e81139882b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7363483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d480f048a2539e88d7d2a6d5331516350244cc0681ef4aa98282ea96763c8b5b`

```dockerfile
```

-	Layers:
	-	`sha256:1568f9aa637437689c6b2426995e08b5900e1fe3a27fe3dd0c00641a9caa3287`  
		Last Modified: Tue, 21 Oct 2025 09:44:15 GMT  
		Size: 7.3 MB (7346993 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ccc64416d147b432955b53932c7018ac5723b970e3465d6141205f51223f9de0`  
		Last Modified: Tue, 21 Oct 2025 09:44:15 GMT  
		Size: 16.5 KB (16490 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-1.12.3.1577-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:977b710523ada388194e6d3df3de9878de6c3fb6ca8490127b76b87e4dcfe3f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.0 MB (212992101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14c647d130a735f6890c1aef6c8e2ce963b2ec8b98d1cb67c0cce5b78187c756`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1760918400'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0a72c4e347b74aa6a0086cf3d1d928528ab02577a17bff4e22366a7df681f564`  
		Last Modified: Tue, 21 Oct 2025 00:19:19 GMT  
		Size: 52.3 MB (52257444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3c222e6636d307070e9cd2ddb2c7b0a9d6d09a84e0a0504596ab238f28fad7e`  
		Last Modified: Tue, 21 Oct 2025 02:30:29 GMT  
		Size: 91.0 MB (91045249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1584ea95b74d9451d38dafb1c3291c7adf9c0f0b8010c6383e23e53919374740`  
		Last Modified: Tue, 21 Oct 2025 02:30:25 GMT  
		Size: 69.7 MB (69688366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68338b52c0cf387eff5c03db2c35747d5ca1e407df845573a685a701733bfa49`  
		Last Modified: Tue, 21 Oct 2025 02:30:16 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83bb4a62b31fb15654b8665cfb7244fb52278e2069e2286a9637cba81506511b`  
		Last Modified: Tue, 21 Oct 2025 02:30:16 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.3.1577-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:17c179659f79a41e8b97918925257c1737f047c1a40f16490eff932202e0faff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7368744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2a475f37c9e7a71a53864b0739b5e95cbc7e170747112876193f65f1477ef40`

```dockerfile
```

-	Layers:
	-	`sha256:9106ac59eb842d73f870f1d5e3223e3382803bdb45a16da647906d9fb43f8ae9`  
		Last Modified: Tue, 21 Oct 2025 09:44:21 GMT  
		Size: 7.4 MB (7352113 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dcacda32797aa38dfe0a8ca0cca0e0f3e7356d4a946622ed7368cee6facb5f3d`  
		Last Modified: Tue, 21 Oct 2025 09:44:22 GMT  
		Size: 16.6 KB (16631 bytes)  
		MIME: application/vnd.in-toto+json

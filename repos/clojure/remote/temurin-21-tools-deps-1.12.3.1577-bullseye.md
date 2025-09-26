## `clojure:temurin-21-tools-deps-1.12.3.1577-bullseye`

```console
$ docker pull clojure@sha256:5fed1cc8782595ca6fc2736b9d16befff51b7d963f90542ead7cd0905aef9db6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-tools-deps-1.12.3.1577-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:3972bff116ef169d4acf6e4191eff333d5911ad14ef48d1b53c2cea7b3b001a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.1 MB (281122328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e1222ae5740e21585b915fb984a2b1a9d0325e8050940ebb0cdd6405bf1b4da`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1757289600'
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
	-	`sha256:035115815e46101f9c9956e02e706f2f3ec8748e2b415f0d232b51eb76a6a779`  
		Last Modified: Mon, 08 Sep 2025 21:12:56 GMT  
		Size: 53.8 MB (53755396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f4c4928543010da6bc88bae88e21d6563a794a9b25dced811f6892831971c41`  
		Last Modified: Fri, 26 Sep 2025 20:01:44 GMT  
		Size: 157.8 MB (157804763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7cbf71127ce0591099b5b5b58dd138a338f41116228e23d21bc6f74323288a0`  
		Last Modified: Fri, 26 Sep 2025 17:57:38 GMT  
		Size: 69.6 MB (69561126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97b8a273b4ddb82d9a4cfa6cdd72a547796872c98f8aae592553ed70e0b7335e`  
		Last Modified: Fri, 26 Sep 2025 17:57:29 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aca4bc5714ed6b1e375a7cc584ed29500f78b2b31bfc1ca0d51f8f057d03ba7`  
		Last Modified: Fri, 26 Sep 2025 17:57:29 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.3.1577-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:85b8f43ae9aee27006ef88b6589aee57c36b7427c6b09f8e1364664745fbc044
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7414590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b7bc28a41a89bbf8f253d9dde7001794e39f421b49a6f06d0eb44e4bf97647f`

```dockerfile
```

-	Layers:
	-	`sha256:46e90c609daed3723adc52af4116d5e5cc6e4c678eb90377bfeb37357547fd00`  
		Last Modified: Fri, 26 Sep 2025 18:41:29 GMT  
		Size: 7.4 MB (7398769 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1fc0c9f09334005a456cb0bafadc14490962e6eb68ea56df9879dfd7ceebf969`  
		Last Modified: Fri, 26 Sep 2025 18:41:30 GMT  
		Size: 15.8 KB (15821 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.3.1577-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:f6e40b466511423cfa911cf7856a6ff72db105ecbbe3bfe5a8dbc75f468e6dd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.0 MB (278018969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:429eb0ce2e0822e36d7bd15828f13104c0082e64c49ba529620e6f402f861c7b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1757289600'
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
	-	`sha256:7df02cb4a974a4e8a9eb65ffcff7274f9dca341d29aaa763294c42e49805ca19`  
		Last Modified: Mon, 08 Sep 2025 21:15:41 GMT  
		Size: 52.2 MB (52248370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cbb5d817a7ab755bf13f36abfc3da40d21d97b5786f87c575375d86418be679`  
		Last Modified: Fri, 26 Sep 2025 20:01:58 GMT  
		Size: 156.1 MB (156081217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a82c30629e2cfddc0d27c8b4c7c6a22d77f61f57f1694b5659c901d2eeb4eb82`  
		Last Modified: Fri, 26 Sep 2025 20:02:17 GMT  
		Size: 69.7 MB (69688342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22fbc7d0f4f8d362dac25a3f712149ff200eac6e8a3fef5877525dde94810bd7`  
		Last Modified: Fri, 26 Sep 2025 18:48:43 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:043e90b0bf2662358cf0f094c25f4398c805df5799893e638095333950527ef4`  
		Last Modified: Fri, 26 Sep 2025 18:48:43 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.3.1577-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:88d487f2e1afb33091453fc21e16e77ecee6f0487dc14e4f8546f12c8fe60bc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7419807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c758bb33f16ebca0ef848206fd3e05c29a685dde01dd4b9922e89d3f1514b80e`

```dockerfile
```

-	Layers:
	-	`sha256:ad9acf8326a210a46fd7753aeaae0ab4ed804fc635b16a1b9dfa4418c0f48c80`  
		Last Modified: Fri, 26 Sep 2025 18:41:36 GMT  
		Size: 7.4 MB (7403868 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1cf3278cd798f870e12ed286c47f9e099d0e4a6162ac213f2ce5889e23281584`  
		Last Modified: Fri, 26 Sep 2025 18:41:37 GMT  
		Size: 15.9 KB (15939 bytes)  
		MIME: application/vnd.in-toto+json

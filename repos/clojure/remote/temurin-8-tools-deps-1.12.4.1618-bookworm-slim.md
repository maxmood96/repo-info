## `clojure:temurin-8-tools-deps-1.12.4.1618-bookworm-slim`

```console
$ docker pull clojure@sha256:b606e9c94b49aa5e5ae7a27d2b09853f2dc0a14b56867a61f211ff547c44ba35
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-1.12.4.1618-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:7aea941b03833e38f895ccca79539e15446be81e02504d0f3db0fdfe7a21332d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.1 MB (153108438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b8a85861f532c2bc6de464b8759230cc8627c4872ad7657a5fb2e073c01a829`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 02:56:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 02:56:09 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 02:56:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:56:09 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 17 Mar 2026 02:56:10 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 02:56:25 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Mar 2026 02:56:25 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Mar 2026 02:56:25 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:6db0909c4473287ed4d1f950d26b8bc5b7b4206d365a0e7740cb89e46979153e`  
		Last Modified: Mon, 16 Mar 2026 21:52:32 GMT  
		Size: 28.2 MB (28236225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4277b26dedec6a4e710fb747cc087946362a748ee944533d09b45b5ef60cd35`  
		Last Modified: Tue, 17 Mar 2026 02:56:42 GMT  
		Size: 55.2 MB (55170146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2060fd3b7e00f35bbdfe6a4cb6b9b6c4953d9beb774770f3e83482d71b270f5`  
		Last Modified: Tue, 17 Mar 2026 02:56:42 GMT  
		Size: 69.7 MB (69701425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ba58034cb475ce00e103a84c103e18a1942436479a7b9fc3fab566d57d2e821`  
		Last Modified: Tue, 17 Mar 2026 02:56:39 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.4.1618-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d65e43cccb072ca2c26e15a169e9d37c2f722b45a02256b12d23c94ff58fbb28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5251402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:595d7b3c3a3c69a9b9d98f6c3a0eea62953dae46b952ad1eefb89bf5d8f09136`

```dockerfile
```

-	Layers:
	-	`sha256:3cc560d504dcd0fcef3441e826595bfd36f7201e21fb9e7f6b64e74cb0f64285`  
		Last Modified: Tue, 17 Mar 2026 02:56:39 GMT  
		Size: 5.2 MB (5237154 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab60fa63e3d5aba3cb005efe87cb2dca61dd6cdd0ba568792ede54b5af908f75`  
		Last Modified: Tue, 17 Mar 2026 02:56:39 GMT  
		Size: 14.2 KB (14248 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.4.1618-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:ad901387d7ed50c8fe988929d93e5477d9dc3e488e8ee0766f5548bb9d7c6c90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.1 MB (152057177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b057972752df89a7648e94a81c1d9ea946f2503468b06783050bee2a86f1817c`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 03:00:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 03:00:38 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 03:00:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 03:00:38 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 17 Mar 2026 03:00:38 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 03:00:54 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Mar 2026 03:00:54 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Mar 2026 03:00:54 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:d997cc310c981ac52155d0d9fe28888b261a7746a3877bb0ca848fd1a83d319a`  
		Last Modified: Mon, 16 Mar 2026 21:53:12 GMT  
		Size: 28.1 MB (28116065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a3e6b072dc22aa4facd9121d8539874cd773fa8479c466607b0e913381c86dc`  
		Last Modified: Tue, 17 Mar 2026 03:01:13 GMT  
		Size: 54.3 MB (54251604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1be058cf3bf87a44d6050e47aae610623a7aea8ed83633580b0b474e8a7ae2bd`  
		Last Modified: Tue, 17 Mar 2026 03:01:14 GMT  
		Size: 69.7 MB (69688863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a692ed3c68f58d28e31346ff867c041045195db1788846f1d9a929369b45e876`  
		Last Modified: Tue, 17 Mar 2026 03:01:13 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.4.1618-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:926e99c9d1ee586d8ea105f2396e1d3ff3407ecc5c65eafb91e0a26c7bf1c623
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5257981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f23e8c4c61181adefdd0b41ccffdc81e3b56c4ca0a89dd521d08450b217ab02d`

```dockerfile
```

-	Layers:
	-	`sha256:acd36bbdc4ee876c89b932b36719c2d9ba69b463e2ddd1feb14c89adda36912c`  
		Last Modified: Tue, 17 Mar 2026 03:01:14 GMT  
		Size: 5.2 MB (5243615 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b05992d60747b97537614860a227e788bf05e237c1382b9dbf455e14b696c6d3`  
		Last Modified: Tue, 17 Mar 2026 03:01:10 GMT  
		Size: 14.4 KB (14366 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.4.1618-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:16253d6f0a6e33f42e58b99399ac893bce86b26a17a57871ffea8f9cc33419b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.3 MB (160262880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0f3f26d7056d7a0e97d9a2daec6185627138ad8317f6498fd8ed6fd82f6b426`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 18:06:19 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 18:06:19 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 18:06:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 18:06:19 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 17 Mar 2026 18:06:19 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 18:11:02 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Mar 2026 18:11:03 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Mar 2026 18:11:03 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:7a0392d98c02d4219c67a8e3d3837c1ac5d4af6836b9264bdd6c427cc7a24f76`  
		Last Modified: Mon, 16 Mar 2026 21:51:26 GMT  
		Size: 32.1 MB (32078368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d87cd97df95540bc764bd675651a228c43a8bd513ce7d2048e612519e294f6d`  
		Last Modified: Tue, 17 Mar 2026 18:07:15 GMT  
		Size: 52.7 MB (52650377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:834f97609ec0860c0497921916bc81aa52f30a37820a38cb43b09fa60a2f401e`  
		Last Modified: Tue, 17 Mar 2026 18:11:38 GMT  
		Size: 75.5 MB (75533490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d5cdb70a8cf08091d585cf88a8109f83a2667943f4a027bb7236ef83df855fd`  
		Last Modified: Tue, 17 Mar 2026 18:11:35 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.4.1618-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:69e68945e7b262a4b174a028d6c42869cd988164b6d7659a3572ab8b30486fb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5257203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f014e0808b3f94cb6d882c88c3c50fd3bb65dece403b80f2efe46b2ee753d056`

```dockerfile
```

-	Layers:
	-	`sha256:189f6890a72d816ef56f42a60d56f3c43597aeecd0e20ca6d1e2a23d0c6c2dd3`  
		Last Modified: Tue, 17 Mar 2026 18:11:35 GMT  
		Size: 5.2 MB (5242907 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aada4c94cefe8fc4de3cc4bfce410751898d90b3381bdec12db7ec39f6edef86`  
		Last Modified: Tue, 17 Mar 2026 18:11:35 GMT  
		Size: 14.3 KB (14296 bytes)  
		MIME: application/vnd.in-toto+json

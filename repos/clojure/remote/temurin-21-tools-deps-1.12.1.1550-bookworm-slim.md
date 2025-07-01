## `clojure:temurin-21-tools-deps-1.12.1.1550-bookworm-slim`

```console
$ docker pull clojure@sha256:cc35c102fcba052b4d8c928cf9492f329ad39c8f292ca204098e474102a3b409
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:temurin-21-tools-deps-1.12.1.1550-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:a962c1a443ba84c893100dd934860f73731a9fc79d3b0d57ed7fd8006cc76f60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.4 MB (255398924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adc16149832aeb13cc3c9456f9abcbfe43edba7fc9db67158de8f30e24bcea68`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3da95a905ed546f99c4564407923a681757d89651a388ec3f1f5e9bf5ed0b39d`  
		Last Modified: Tue, 01 Jul 2025 01:14:43 GMT  
		Size: 28.2 MB (28230143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:325d75b842fa7e353f9885eafdf166a3391746bec919849809a3982c773e78db`  
		Last Modified: Tue, 01 Jul 2025 07:04:24 GMT  
		Size: 157.6 MB (157634498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90f557a897ca05570e518125ec89eeb4ab10f4abb6922c52ca01cee61f83f689`  
		Last Modified: Tue, 01 Jul 2025 07:04:09 GMT  
		Size: 69.5 MB (69533243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27fc122f77c88e2a37f249853dd8e45d89f6c0daeb3cfc02ce4b231483af3443`  
		Last Modified: Tue, 01 Jul 2025 07:03:58 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a269bce268a055e4c8ecc27ec52c5e8e992621e60291016b19c10e7f72f7218d`  
		Last Modified: Tue, 01 Jul 2025 07:04:01 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.1.1550-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:14899dd0f0b8ee75e87fe5fd695a2ac3cba5f106b2f277dcd33bf306d573f7ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5131617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e599b8c099d758ad71153a85c159c4a6d1edce89c8a8cf5996b9fea676ff43b`

```dockerfile
```

-	Layers:
	-	`sha256:200273b45c11f1b2ab1daae898ca6045b58c1d02b1caf67bac29068a6cc50a83`  
		Last Modified: Tue, 01 Jul 2025 06:38:45 GMT  
		Size: 5.1 MB (5115042 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36d7ecea997681f549eef9a97419e25954f43fe400840937da87e17a670203d3`  
		Last Modified: Tue, 01 Jul 2025 06:38:45 GMT  
		Size: 16.6 KB (16575 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.1.1550-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:9ffea213d5a690efc509949d3520536631c6ac0a9897b1e9e3eceaef0f6280aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.4 MB (253396091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d94c41199c40e1bb3bcae78d4ed1d77a619958334a52e47fa61dca29cc3d8494`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1751241600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:37259e7330667afd74c3386d3ed869f06bd9b7714370c78e3065f4e28607cc02`  
		Last Modified: Tue, 01 Jul 2025 01:15:09 GMT  
		Size: 28.1 MB (28077678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3acac392c98990c320593217a0d8bd8d0ffd8c866d1992689a7186665231aa3`  
		Last Modified: Tue, 01 Jul 2025 12:27:52 GMT  
		Size: 155.9 MB (155928844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:512eeb512f8d9187eade339476e6eb962073ed849ce329671e26f94d6a63ac40`  
		Last Modified: Tue, 01 Jul 2025 12:54:14 GMT  
		Size: 69.4 MB (69388531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9633a1f6118614cad10fed69aaf785a4f38a0275871a8f5042abe173c777241f`  
		Last Modified: Tue, 01 Jul 2025 12:54:10 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4213bd6c11bbc7ebcfe32aac52ad03ed005350b6596eae8f9f74a4a538bfe1c7`  
		Last Modified: Tue, 01 Jul 2025 12:54:10 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.1.1550-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d5f10fb32254207d0f993ed058c9330c23b932fa23e99496873b257e424c1dac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5137544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef8a8fa66cb6a01e7796cbe27536206635153186fb4ea3298b00f35b5171a140`

```dockerfile
```

-	Layers:
	-	`sha256:51e7398d81ab4235ef22441022b7799f7998a261686e9834b4aedd43f3e79d79`  
		Last Modified: Tue, 01 Jul 2025 15:38:25 GMT  
		Size: 5.1 MB (5120827 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3b1f54bd50dd974cd7bfd6931cf2d728edac2ff0205c71ca758fc40199daa46`  
		Last Modified: Tue, 01 Jul 2025 15:38:26 GMT  
		Size: 16.7 KB (16717 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.1.1550-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:7d0aed9253dfbf4c2b25b226a500e4fd7d2b985ac4380f892e3ae7e7977d2a9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.2 MB (265236679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3cac1387a40fd30760f6cf1b6b40aae71814bb77109f5580adb069555914980`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1751241600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c5884d20b08634214a92bd5de559876bf30e6c5453807c3014f5480eeba20662`  
		Last Modified: Tue, 01 Jul 2025 01:15:20 GMT  
		Size: 32.1 MB (32072820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a38654763bb3a63922902695f120b682d664a012fcc0d772bf4d0ef943e45880`  
		Last Modified: Tue, 01 Jul 2025 13:21:46 GMT  
		Size: 157.8 MB (157804904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47a3329b1d5937bb0df91c6682f89b503048a1aedee95912689cb64395563015`  
		Last Modified: Tue, 01 Jul 2025 09:04:34 GMT  
		Size: 75.4 MB (75357918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:884ee21b0b1f417255b4f140560b0bfb768585c9b40ab70b5292a5b5c9c94caa`  
		Last Modified: Tue, 01 Jul 2025 09:04:26 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34daaa86378fd8a52da12d1a74acbff73a2bb25937d753b588f45ca684513ecd`  
		Last Modified: Tue, 01 Jul 2025 09:04:26 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.1.1550-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:2c7ebf6843ddb5eafb691cb27ad8d753211a297ba3102ba6b0dc1c4aa6d6e5b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5136847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41b54a6ada4fbdd31aee7b1d43a7c939cc8510c5c88254ba259837ac148a5c69`

```dockerfile
```

-	Layers:
	-	`sha256:e2736071e86ee6b659db03193346708ce9aa3b8137b2edda29142ce96cb36e1c`  
		Last Modified: Tue, 01 Jul 2025 09:39:50 GMT  
		Size: 5.1 MB (5120212 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29d6fe63aa161555b1b0175286e679e3cb1f6f9f304c105ddff583b6d35f1710`  
		Last Modified: Tue, 01 Jul 2025 09:39:51 GMT  
		Size: 16.6 KB (16635 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.1.1550-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:d78f57a6e7ab00893952035834a99d2fea0eb85d096bd300d26b78dc6864f1f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.1 MB (242138211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d01cddb68bd034bf1c39ba54944c9c4c2942ec90aeb52c2e97fdcad8cdf42f5`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1751241600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:46b41ca6e821ec27aa0ddf43e603c69ca49f20e377997e4087ed991c9635aa70`  
		Last Modified: Tue, 01 Jul 2025 01:15:56 GMT  
		Size: 26.9 MB (26887811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a78851f8d34d14662daf39001acd8755a64fb3dfba22433fc87fd415cf349eee`  
		Last Modified: Tue, 01 Jul 2025 13:32:20 GMT  
		Size: 146.9 MB (146910994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaafaae62ab8b5c942cf0c2f04fce73b7bc243fd95ff4bc90f0e27b34034e282`  
		Last Modified: Tue, 01 Jul 2025 08:22:02 GMT  
		Size: 68.3 MB (68338365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a76c6cc2d98db365766114ba89281eab1012b933cfdc825114ca212fdb8fbc3e`  
		Last Modified: Tue, 01 Jul 2025 08:21:59 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b30f0b52bdd3e218f2c73136851a7c9cc3468a679b7b704f47ea468730d94fe`  
		Last Modified: Tue, 01 Jul 2025 08:21:59 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.1.1550-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e2a9fb8b72ad7994400d0c325a2d00f03902366f6d77d068aede0275ec33fb7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5122938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74ab1213625d8259719a082da87b24d74d50723812cac3ed1b5e51feccb5085c`

```dockerfile
```

-	Layers:
	-	`sha256:096f4b58e192f2f16b8ed26b3a966e86c3dffb08649c045efc087e950f667dc0`  
		Last Modified: Tue, 01 Jul 2025 09:39:56 GMT  
		Size: 5.1 MB (5106363 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6f569f4636ee4389d2d6eb230f795c9be6ea055318829f698bed98ce1d36c0b`  
		Last Modified: Tue, 01 Jul 2025 09:39:57 GMT  
		Size: 16.6 KB (16575 bytes)  
		MIME: application/vnd.in-toto+json

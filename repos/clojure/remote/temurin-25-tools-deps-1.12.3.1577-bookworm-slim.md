## `clojure:temurin-25-tools-deps-1.12.3.1577-bookworm-slim`

```console
$ docker pull clojure@sha256:f92f4fa16a26a864a1fca0a2cb2f95faa3d54bd154899ea6347d0676ee689fa3
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

### `clojure:temurin-25-tools-deps-1.12.3.1577-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:6620c6aa2cf1aa3c9903be40236f2b8452f79c6fcbc17b20fb33269083d3e2d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.9 MB (189944834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e89c4064ccd069f585d7979db9e2253cc051cb2c3b84430cc2d612c56ef1f900`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1760918400'
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
	-	`sha256:abe1fea375429ba91b23776f15f53da4ed790fa2b779b40d20f21e69bd66de5a`  
		Last Modified: Tue, 21 Oct 2025 00:19:19 GMT  
		Size: 28.2 MB (28228321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d39b4cfa73cad3d448b49a2410a574b7cfadbbf8911a446c19adc30daac16ec6`  
		Last Modified: Tue, 21 Oct 2025 02:24:47 GMT  
		Size: 92.0 MB (92036051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b5e5e7af3b115d13e6196dff772b8702a8387cc681e36272c51c7463c90d953`  
		Last Modified: Tue, 21 Oct 2025 02:24:45 GMT  
		Size: 69.7 MB (69679420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58ece98cb1104b7e33d915f082bcbbad2d87fe1077fa50de7ea3b0e0550cc229`  
		Last Modified: Tue, 21 Oct 2025 02:24:37 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2367096cde73233376d078d03f4d57b6e7038e5a67f7affdee4995fed5b6b0d`  
		Last Modified: Tue, 21 Oct 2025 02:24:37 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.3.1577-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:769c1a205f85b172aa647f32d808eebb227f1278fba90b127c5a5aaeed90f459
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5081302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61209f764652f48cd6b47cbe76c576bd192d077a05f140ea3f53c9b6a3e17ce3`

```dockerfile
```

-	Layers:
	-	`sha256:60804d50ec3a5c5c1fec79331ebc608f7589756b0fce50a6d49a0c5ae54da2d5`  
		Last Modified: Tue, 21 Oct 2025 09:44:06 GMT  
		Size: 5.1 MB (5064734 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95ce4285448db91915a895d10dbf86fec3f5f4275612e75decbd41255de3d87a`  
		Last Modified: Tue, 21 Oct 2025 09:44:07 GMT  
		Size: 16.6 KB (16568 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-1.12.3.1577-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b6a7b4d572fab09f00bcd596cc29f4900f7e48a77495fa674dad0d02bea972dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.7 MB (188708919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65aa22ff13770c8bd87eaae4034cf8f6f07e4953af5f899f407222f5265c2ebd`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1760918400'
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
	-	`sha256:21b7accdc53fc02b56a5c1cccd412be04189e5a5e674fd092ffbedc72596be91`  
		Last Modified: Tue, 21 Oct 2025 00:18:57 GMT  
		Size: 28.1 MB (28102190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7211226d28718128b0ac1f3ce0b249b63e2c8ac4fa51aeb1dfcf4895b3c79c08`  
		Last Modified: Tue, 21 Oct 2025 02:29:52 GMT  
		Size: 91.0 MB (91045250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50d3ecadd6cfe7cb6238df99f6fd8ec9f2d5a8cf3b765c3792821bdde501662a`  
		Last Modified: Tue, 21 Oct 2025 02:29:51 GMT  
		Size: 69.6 MB (69560437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bebc7493e868e3afe6d9eb80377f06c316ff390ca0df0b30d5c19f8b0b82424`  
		Last Modified: Tue, 21 Oct 2025 02:29:48 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e47a8ae3ff3f52f9c8a1280013ea6cbaf5adc7a0f2080c05c6fbb60bc2da5789`  
		Last Modified: Tue, 21 Oct 2025 02:29:48 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.3.1577-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:21c3b8cb436c7078e57991789fb8617a1dc65bdec295fc8c1be3ee0bab400246
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5087226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a57e27ff71dfcd0aa813839f7c168171022efccd47926962d7b7a6fab90d33f3`

```dockerfile
```

-	Layers:
	-	`sha256:380d6f8d66ec61ea882dc3a0688632b17d14690e91fc183d3163644a21195a3b`  
		Last Modified: Tue, 21 Oct 2025 09:44:12 GMT  
		Size: 5.1 MB (5070516 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e0cd5f070fd8f27b1deb55e5ab9a1081f1f08259bda674059347033c065c004`  
		Last Modified: Tue, 21 Oct 2025 09:44:13 GMT  
		Size: 16.7 KB (16710 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-1.12.3.1577-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:869854c32800d4384336fc5f3e1ef866d2e8d17e18fb229149fddc6fe4285158
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.2 MB (199184555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dc1cb98573727f800347b74028f9974d06839a536bb6e595608f0df00c504f6`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1760918400'
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
	-	`sha256:5a28d569c39dc949a4743122d7b5ec2d2e0664f1276c801bf984a711d80f2a1d`  
		Last Modified: Tue, 21 Oct 2025 03:26:43 GMT  
		Size: 32.1 MB (32068780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00eea9732a9b3df909d8096a50208d51fe27e25ac611f0c013be9313c9a3d7ec`  
		Last Modified: Tue, 21 Oct 2025 16:18:36 GMT  
		Size: 91.6 MB (91601717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:531931101b806ec086ab928513c2e632dfbf4d3f89a111af0921f37242f2212a`  
		Last Modified: Tue, 21 Oct 2025 16:25:26 GMT  
		Size: 75.5 MB (75513017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0569d92647d34e631dbe0b3e849151a4977cdb85384c61c06ffcae7ff3efa22c`  
		Last Modified: Tue, 21 Oct 2025 16:25:19 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f537404e4af997f454bb1f448848878520761921668bd4c1141377bd6b842fd5`  
		Last Modified: Tue, 21 Oct 2025 16:25:20 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.3.1577-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1207550149498c9a3448e7c21bcfcec588b8140082b733d6e68e43f52d7bc4fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5087830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9142bb7b94a7b9359fc6784e474c2ecd178f8646ca5a86fe56e8ce71e0d17472`

```dockerfile
```

-	Layers:
	-	`sha256:18d19ff89cedb87f4ae0ccfa9e85c75c8c0978ef745dde7fdb524e9ce49db539`  
		Last Modified: Tue, 21 Oct 2025 18:40:31 GMT  
		Size: 5.1 MB (5071202 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c3d79fa8f8b02db760b3fc08371fb070135bf5d588e4fa7203a2e4abd7240de`  
		Last Modified: Tue, 21 Oct 2025 18:40:32 GMT  
		Size: 16.6 KB (16628 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-1.12.3.1577-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:2ba6290ce4e22cf786be2035e8355e3c903b5a23083df074bd4b016416b2cccc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.6 MB (183581898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8279f1f8d8f7e3e474fe5b12b5b43a8d565d2fee118d2ac7097311417f7245f7`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1760918400'
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
	-	`sha256:43b0f588b497b17691a3547afa4ae41853829cffde6930e6425ddae4a3f89278`  
		Last Modified: Tue, 21 Oct 2025 00:21:28 GMT  
		Size: 26.9 MB (26884356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c941c3171e3f06378348541053cdf3a39f45e15fb4693ccf079d3be12238d423`  
		Last Modified: Tue, 21 Oct 2025 22:42:41 GMT  
		Size: 88.2 MB (88206427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:004581b56a9cc5ac3e8ab0518e8fc0b11934666c024c6b5599205710cb30b8bd`  
		Last Modified: Tue, 21 Oct 2025 22:46:53 GMT  
		Size: 68.5 MB (68490077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1a993cfbbb5ab3024c1007c11ab7c159c0395e985a0329fe642c4145f397557`  
		Last Modified: Tue, 21 Oct 2025 23:00:30 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30411e67960be5016e52c833a7a34858abca2d7e0bc88db0e2dc92818b831263`  
		Last Modified: Tue, 21 Oct 2025 23:00:33 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.3.1577-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:f72b4b889a3c4afd8851e52b4bbdef34cf7e791bcca18deb1cdbe6e9ced30f64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5075170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5c9b59677fc11d052bb74f96813b6b69258d250577d98c66b8dcfec424b7932`

```dockerfile
```

-	Layers:
	-	`sha256:cf51e69e2c55ccb8928da83b068ec96307281620c7119bdb4880407ca9b60f50`  
		Last Modified: Wed, 22 Oct 2025 00:40:21 GMT  
		Size: 5.1 MB (5058603 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15a26e6bdb3937cb6a357af9d43ede7a5b3073fd11e0d1051a74ec36a72f07b2`  
		Last Modified: Wed, 22 Oct 2025 00:40:22 GMT  
		Size: 16.6 KB (16567 bytes)  
		MIME: application/vnd.in-toto+json

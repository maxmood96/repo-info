## `clojure:temurin-17-tools-deps-1.12.3.1577-trixie-slim`

```console
$ docker pull clojure@sha256:a8cf6e4f0f695bef3bfbf68f3e2696dca87663f55d7f0059e08b43cf88a65685
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

### `clojure:temurin-17-tools-deps-1.12.3.1577-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:2edf216fdf6682b064c00ecea95b9154a7f41412e94106e77c6261a0a4c2fca1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.4 MB (249410615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeaa4ed45a68d59886b69368737c5be459d731d7865a1659ab4758e9fc9370a6`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1759104000'
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
	-	`sha256:8c7716127147648c1751940b9709b6325f2256290d3201662eca2701cadb2cdf`  
		Last Modified: Mon, 29 Sep 2025 23:35:28 GMT  
		Size: 29.8 MB (29777766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bd4a6ee8399e3f19028dc8f9b20882f0c866332462481abea023b601dda6d0a`  
		Last Modified: Sat, 11 Oct 2025 03:29:49 GMT  
		Size: 144.7 MB (144693312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2d96e9cf09297d4bef70f6d079dd5882e1686910c8685a2f709f8214b3c2167`  
		Last Modified: Thu, 09 Oct 2025 22:29:09 GMT  
		Size: 74.9 MB (74938493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:875f5a36e980eb59d246e9da85a3abcd0f05658b99b6c3fe997b475eb7f9a3bb`  
		Last Modified: Thu, 09 Oct 2025 22:29:02 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33499c934cc40b609f60b22ab8ac371cd87d347f70af56cd6517134474deedb3`  
		Last Modified: Thu, 09 Oct 2025 22:29:02 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.3.1577-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d062492e55f4e4b99815067525c860f0a8b5a7d82f73adb6f2c407e3d463543f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5272022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e50a0406fb8b920317a6ac9407a67715dda63527c2ca8255823758be7d5525c`

```dockerfile
```

-	Layers:
	-	`sha256:02e4cdf606cdf19b0c7f60b26cfd5e04903c83ed2a33859b81859dbd935bcac4`  
		Last Modified: Fri, 10 Oct 2025 06:42:46 GMT  
		Size: 5.3 MB (5256167 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:edb32118a6012198c0ac014beb4c6179aeac013db71c29153d192226f23e4526`  
		Last Modified: Fri, 10 Oct 2025 06:42:47 GMT  
		Size: 15.9 KB (15855 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.3.1577-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:7313ec848e1aa12f750e8feacc44cda7ca5cc6664dd4d4bdffb573a7b1116636
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.8 MB (248808692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e695529e84101f74bb6d4a45a51d96e929129c8a36dfd7b660d24a91fa441b5`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1759104000'
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
	-	`sha256:e363695fcb930d5f18449254c0052117582c3de4263c91575b0a9040c986e412`  
		Last Modified: Mon, 29 Sep 2025 23:35:13 GMT  
		Size: 30.1 MB (30140842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b907373632f6f73c6f52758095569093be634487c9c5181a951fb29bad5b95f`  
		Last Modified: Sat, 11 Oct 2025 03:27:14 GMT  
		Size: 143.5 MB (143542161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b5df64e70d5d690681bc60894413429894e9d5c92cd4fdd7bb293b7779fd02f`  
		Last Modified: Sat, 11 Oct 2025 03:30:19 GMT  
		Size: 75.1 MB (75124645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13adc5f7b2f20310c9b5e3aabf4b598c8c399a22322863bdc12194e719544de9`  
		Last Modified: Fri, 10 Oct 2025 01:41:02 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:affe6c7fe348b70807187a4963f50993b04aa2d5a50e468ecb1d045f582aeb9a`  
		Last Modified: Fri, 10 Oct 2025 03:47:02 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.3.1577-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:976a35760ff5f368f8e394dd89d12d6db9d85af32e77975dc174d14c1e4c5447
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5277909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a16e82f082011e80d49046116b590988e22004f4c7e0567b09655916b1e9cec`

```dockerfile
```

-	Layers:
	-	`sha256:0da1ff80b7560ab0ad5ffb61ddc0da224b6ce97d4fe60a4b4279538a29877e8d`  
		Last Modified: Fri, 10 Oct 2025 06:42:52 GMT  
		Size: 5.3 MB (5261936 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:249ec9496eb385bca4c0e6ffa477c220e8e97efdfe287c3cd318d1511fb6f5de`  
		Last Modified: Fri, 10 Oct 2025 06:42:52 GMT  
		Size: 16.0 KB (15973 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.3.1577-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:aa51895e0d108421ad429a36a63f45fcaaadcf348723dceb73473ef18c358bf5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.6 MB (258560510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e41e38105e37758ba16adc98e596bfa46ab4a217795bd64b111c2646c0f40a34`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1759104000'
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
	-	`sha256:8bcecd3ced4047f6a4d35464fc2ee9b45e7fcc10b49690427794f4421b0552ab`  
		Last Modified: Mon, 29 Sep 2025 23:41:19 GMT  
		Size: 33.6 MB (33598454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cba05d3e1f82aa7350de29683542014410151ba5da078d43d5651f61d1cd89b`  
		Last Modified: Fri, 10 Oct 2025 05:22:47 GMT  
		Size: 144.4 MB (144372884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d79e0cfd3f1315366f3b18972071aa9ddf9ceae8c87942e4cf9b2e17de70d34`  
		Last Modified: Fri, 10 Oct 2025 05:32:17 GMT  
		Size: 80.6 MB (80588126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7e7ee4e8abf28393b3e8454fa43fb505bfd58058714f1e77aee29391ba8279a`  
		Last Modified: Fri, 10 Oct 2025 05:32:13 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b83f727539bf46f3d2c2da2b79ce1414efb8e383e32d3d386c8d1a5d6d0e562`  
		Last Modified: Fri, 10 Oct 2025 05:32:13 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.3.1577-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:3a4a3e55334929c53f3503e528b464615f34e29ddd1ac94cb6f72340b04b88ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5276441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d972a9c72b78f6941755d567dfb82367e96905b624782ae9e1178a445150dc5b`

```dockerfile
```

-	Layers:
	-	`sha256:157b19a86a63b869ca3101a48018012a29ec6a8b9a0233e41cff59127a0cb251`  
		Last Modified: Fri, 10 Oct 2025 06:42:57 GMT  
		Size: 5.3 MB (5260538 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ab9dbf6c6fac2adf12662208b0c502224547af96d45cc8d45756b21d40d5251`  
		Last Modified: Fri, 10 Oct 2025 06:42:58 GMT  
		Size: 15.9 KB (15903 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.3.1577-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:5d586e0f15efe6d249ae33a1cec12daf361126569874798a3f0696d87dea59b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.3 MB (240340644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05e79462d18df539d5fb271f8823e33cb94fc041d2c718a8dbe489deeec393de`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1759104000'
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
	-	`sha256:ecc6f9aec21fb94a493c2875c244e720a2f7c6c034063ce87b2f5b6b46962ec9`  
		Last Modified: Tue, 30 Sep 2025 01:05:14 GMT  
		Size: 28.3 MB (28275502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43dfb1dd1350f7a95ce53ab9177ca67c179a1680059cb360645b0c6008226957`  
		Last Modified: Thu, 16 Oct 2025 07:40:42 GMT  
		Size: 138.6 MB (138575657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33aeeedb75ee546155058752c86a5550795879cbd57e6b310ac287eb8b5b0cd0`  
		Last Modified: Thu, 16 Oct 2025 08:02:18 GMT  
		Size: 73.5 MB (73488440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12002bebce79841f50ec01bb0cea316e21472883a359c85b72fee6af75bff6fd`  
		Last Modified: Thu, 16 Oct 2025 08:02:12 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4ef9066e1f7355aec2a990f44d13357a986a73a76c5febdd78bf10111fb6834`  
		Last Modified: Thu, 16 Oct 2025 08:02:12 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.3.1577-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:0c46d29956ac61b7b70fb267e3a4da2d93ccefed419c948a0c038d7b09d6d1f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5259615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e165947d87b3a7eb669c69836056a7a3b551d7dbc43e17355e428ac0c1b1b85`

```dockerfile
```

-	Layers:
	-	`sha256:f60bd8d4ddd3ff29156cf2fee7417a1e2463b437a0a8fcdaacfd625e61389fbf`  
		Last Modified: Thu, 16 Oct 2025 09:37:10 GMT  
		Size: 5.2 MB (5243712 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:162f1207d57af72c6ffa30b4164d766446f493871195a320df73e514582ed65e`  
		Last Modified: Thu, 16 Oct 2025 09:37:10 GMT  
		Size: 15.9 KB (15903 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.3.1577-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:982f88aa6acc082b1be9dc086d2c18ef9c910ca823295a3665b7f5da201d142d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.1 MB (240125194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50c76604a448df7ddd685f0824ada6c8b49e7cd87acdf09c5ba76119d13be04c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1759104000'
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
	-	`sha256:924b0740f35a15fc20142be5c392f6b033c8051daecf16d2db38c22d6d73eb53`  
		Last Modified: Mon, 29 Sep 2025 23:41:29 GMT  
		Size: 29.8 MB (29837230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a273f5c9c3ebb0cfa0ce46495a97571c2fbd1b6027c2ffebbdf7f10520a2e627`  
		Last Modified: Thu, 09 Oct 2025 23:12:50 GMT  
		Size: 134.7 MB (134723655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ca5571cf2da1e2cd85e19fd0282c541c2aaa0e817e8da19fdf5ef046dbcd67a`  
		Last Modified: Thu, 09 Oct 2025 23:18:23 GMT  
		Size: 75.6 MB (75563267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91caffb0c2132c82952a916c04629d25476369f18e286487eb6994e236227292`  
		Last Modified: Thu, 09 Oct 2025 23:18:19 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1469c4c0a2904700448d77e0bc75eac2817f02c0696f823605563fb3540a1d36`  
		Last Modified: Thu, 09 Oct 2025 23:18:19 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.3.1577-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:03372e5050df5efc8849be00b28cdd9fe253425518b9bd94c21dfaeab00f008a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5267945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:720c93b044129d35d108cdbc30fe98ae13ae93f19dde685248fc179ce4a18e89`

```dockerfile
```

-	Layers:
	-	`sha256:33007678471fe0f0932637f02b33546f6448fc73daae4ae56a94ef3fdf67f14f`  
		Last Modified: Fri, 10 Oct 2025 00:38:57 GMT  
		Size: 5.3 MB (5252091 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4d2adb4e6ded1a99c482b9022addd7d3caecc715284e68d028e26187920bad8`  
		Last Modified: Fri, 10 Oct 2025 00:38:59 GMT  
		Size: 15.9 KB (15854 bytes)  
		MIME: application/vnd.in-toto+json

## `clojure:temurin-21-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:065226173f7facc1066e1c04110fa083f1c654a280301f979e6126c41f6a4725
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

### `clojure:temurin-21-tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:7bac08f920adfe46830ff59b57304ca151a485bd5befa0e9284795d6e3c3de14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.7 MB (255735111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93bb65ccd2e70948879e28adcb3d0a43629a4866d7f495a6316d3da621d097c4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1762202650'
# Fri, 14 Nov 2025 00:54:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 00:54:37 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 00:54:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 00:54:37 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 14 Nov 2025 00:54:37 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 00:54:50 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 14 Nov 2025 00:54:50 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 14 Nov 2025 00:54:50 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 14 Nov 2025 00:54:50 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 14 Nov 2025 00:54:50 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1adabd6b0d6b8acfa4ad149a984df0977135a7babf423538c7284a02744a4ee8`  
		Last Modified: Tue, 04 Nov 2025 00:12:15 GMT  
		Size: 28.2 MB (28228567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b71f90fc47b8e56a1e39a260d22ecc85ef78616aa697bee6dba550ca2b059ae5`  
		Last Modified: Fri, 14 Nov 2025 04:53:04 GMT  
		Size: 157.8 MB (157825975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0282b58bd1400c0795cfb6a3c3c06cbbaa0aec4d31e4cafdd9cba101c328b33`  
		Last Modified: Fri, 14 Nov 2025 00:55:26 GMT  
		Size: 69.7 MB (69679527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fce5758af65551e3e64628b94678277ab87683090685bd72a0c64db3a30e24bb`  
		Last Modified: Fri, 14 Nov 2025 00:55:18 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f084664bab43f0fb26eb5e4db1654e5895b687c243fd51f5ea9c09f8cae57688`  
		Last Modified: Fri, 14 Nov 2025 00:55:18 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:8c4b69510dbf21b9c30d29998287d29fa292aeecee7dff4c7c38e1e30bb1fb4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5132328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:803674b9cddfceaa099aef59fffcdeed79637389d581eb5b7d34ad0e1e23f9fa`

```dockerfile
```

-	Layers:
	-	`sha256:64031bb03fcb9611734e9ef29e98fb63dd52b4f68ec5b26ade708e190ca7e749`  
		Last Modified: Fri, 14 Nov 2025 04:38:48 GMT  
		Size: 5.1 MB (5116492 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d441ef1629560a1a4c99ab5c04db5fe12e4adcfb09fb3eee97a7e5b98ebbc62`  
		Last Modified: Fri, 14 Nov 2025 04:38:49 GMT  
		Size: 15.8 KB (15836 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:2f00f84b2dd8de8b70dfe1a46469ce2d0284e3a31bcdd2799f604422472c3332
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.8 MB (253771467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc4e452f0b0f912b95c2cf81f9bff2ac6508d651ca3a35097d2278b7250a579b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1762202650'
# Fri, 14 Nov 2025 00:56:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 00:56:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 00:56:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 00:56:51 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 14 Nov 2025 00:56:51 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 00:57:06 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 14 Nov 2025 00:57:06 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 14 Nov 2025 00:57:06 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 14 Nov 2025 00:57:06 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 14 Nov 2025 00:57:06 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:162e72af9357868b8f7f48fbf3ea23ddd179a309a9f28f2802a2e785239ec09d`  
		Last Modified: Tue, 04 Nov 2025 00:13:06 GMT  
		Size: 28.1 MB (28102376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2132c24fc654a76482968a9bbce35b966b96c04a2070dbd22cb879e232dcec82`  
		Last Modified: Fri, 14 Nov 2025 05:05:07 GMT  
		Size: 156.1 MB (156107671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f26757336983a376f0204db7f1654bac2508e6104ce8b4f62b895aa0c4e59aae`  
		Last Modified: Fri, 14 Nov 2025 00:57:41 GMT  
		Size: 69.6 MB (69560379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:756aff4558242666cee227fa9394748fc6be233c93af9a7291600ef0c28a8d1a`  
		Last Modified: Fri, 14 Nov 2025 00:57:36 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd8061def0d2fe93e43f8088c3605f824527b03bd06a44f08b70d51a887af7e0`  
		Last Modified: Fri, 14 Nov 2025 00:57:36 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b32127addf79a7e80dafd7349f07eaf3bf93da09729005decf8939ca82e3d77d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5138207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80949ee67426c23c036d7dcd95a09db8ecf85b7bac17875a18c9edc477c32abc`

```dockerfile
```

-	Layers:
	-	`sha256:3ade4acc28aec13448325f01c91fc14408b1cfff7ec028bab76cfaaa8d95e4ae`  
		Last Modified: Fri, 14 Nov 2025 04:38:55 GMT  
		Size: 5.1 MB (5122253 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6150efdb3ff02e14a525bd43c8ec52da66040fad1779127b8f924e317f18c03a`  
		Last Modified: Fri, 14 Nov 2025 04:38:55 GMT  
		Size: 16.0 KB (15954 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:b12a215bfb8a39c36fb056ed06fb4a5d968bc18488193c685256d82de4954f44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.5 MB (265526201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:756beb3b3a8e89767bbce8f80d6065ffc5495a1d8e67262eb510501832edfbcf`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1762202650'
# Sat, 08 Nov 2025 21:31:35 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 21:31:35 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 21:31:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 21:31:35 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Sat, 08 Nov 2025 21:31:36 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 21:39:48 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Nov 2025 21:39:49 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Nov 2025 21:39:49 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Nov 2025 21:39:49 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Nov 2025 21:39:49 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:2442ae4ed78d32124d4f8b92ec0b1caf0e12483bafbd1803659dc391d3600616`  
		Last Modified: Tue, 04 Nov 2025 00:13:59 GMT  
		Size: 32.1 MB (32068905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:944218b16390f9d8d7ad4ec3d5e2b435f5ce7651679065a781dd9f5140c7a7e0`  
		Last Modified: Sun, 09 Nov 2025 16:14:21 GMT  
		Size: 157.9 MB (157942933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6e922bd26c61ac028a26e9066d9b8301e8240a4b7b170ecff6f3244a3873a21`  
		Last Modified: Sat, 08 Nov 2025 21:40:37 GMT  
		Size: 75.5 MB (75513320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c0b93f29b7d504a0aa2630dedd1c1d66f30621b199c8bde5afa7b709eaa2cb8`  
		Last Modified: Sat, 08 Nov 2025 21:40:31 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba724ab1d0fc6b5808a1df80e7eb5aa0bd6ad900be1724b0b9d54429009ef47f`  
		Last Modified: Sat, 08 Nov 2025 21:40:32 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e1e7020c2c25b67632cee34cc4ec1e92f4c7708f0e7083dd38cd89edc9c7d67d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5137534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a221716abf52bc833535f8114b23e835f35767fc6d51eb179dc6c4b0b960dc2`

```dockerfile
```

-	Layers:
	-	`sha256:74a33e6e570fa7f92e52e6ff574b2e2384b68fab57bb9bd35f0afe0637b9ebe4`  
		Last Modified: Sat, 08 Nov 2025 22:46:17 GMT  
		Size: 5.1 MB (5121650 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e7cf5f796be7cd009571f2db601073859f28cccd07fd72be29b1fa449b2c747`  
		Last Modified: Sat, 08 Nov 2025 22:46:18 GMT  
		Size: 15.9 KB (15884 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:f38f41c21720457868ca2708e56d2daf6f73af45423f1d510e4e02c142ee7671
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.4 MB (242446223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1119f2f83992fdfb488d3a57e2c760544191bcae38729b44944d91aa74e5e37`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1762202650'
# Fri, 14 Nov 2025 00:59:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 00:59:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 00:59:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 00:59:25 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 14 Nov 2025 00:59:25 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 01:01:22 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 14 Nov 2025 01:01:22 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 14 Nov 2025 01:01:22 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 14 Nov 2025 01:01:22 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 14 Nov 2025 01:01:22 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:4107e012a4177a1e96e325eb10e9dcf20c399a18fb04e8ea0ee134870259b436`  
		Last Modified: Tue, 04 Nov 2025 00:13:09 GMT  
		Size: 26.9 MB (26884551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:001962ac540e5f4924816e58c77a53181ce9dd682f678ed1b57d3b8615d15054`  
		Last Modified: Fri, 14 Nov 2025 02:06:36 GMT  
		Size: 147.1 MB (147069871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5929eb6bfb2c6196eb1e66bdd7e01636bf452a039fc92e00f14a22a2876a4a98`  
		Last Modified: Fri, 14 Nov 2025 01:02:00 GMT  
		Size: 68.5 MB (68490760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:186e709260bb9335c8c33281ce382d034252ecbfc73e0c6dd3b2cb6f96cd5ccd`  
		Last Modified: Fri, 14 Nov 2025 01:01:50 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b78b8a2969d22916d56d1877aeb048eb0d0a470def325ab7b3243cd4bcac552d`  
		Last Modified: Fri, 14 Nov 2025 01:01:50 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a68a79397047ef34524de983dc845f48b6a4fa276f9c60f460b79417e6c0067f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5123649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9c1806010feb1698df7d82c1ef58014193fd8af52ae0a574e47e1bae9b5d397`

```dockerfile
```

-	Layers:
	-	`sha256:61fe965cf6e46eb9258afc797374f371bcbbd5a1bbf7d55673cffb2900742e9b`  
		Last Modified: Fri, 14 Nov 2025 01:44:54 GMT  
		Size: 5.1 MB (5107813 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7cb61d1843363383a74d1af1b3a48f4f51d8d90b5eb841f7d5817a61e78e6c1c`  
		Last Modified: Fri, 14 Nov 2025 01:44:55 GMT  
		Size: 15.8 KB (15836 bytes)  
		MIME: application/vnd.in-toto+json

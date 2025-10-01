## `clojure:temurin-21-tools-deps-bookworm`

```console
$ docker pull clojure@sha256:267bdebd24818b38c927dec83ee04901e10fcde0ea36fe001d6cc677dbb6a0a3
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

### `clojure:temurin-21-tools-deps-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:f5d64a1040f589ce24e50e24628db6e23ebbf71044de35bd3cf1712b73e7bacb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.4 MB (287431577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:206bdf30c7ad276548b08e1aa955b684415b0ba6253f0968b2a63aad2c1bfd8d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1759104000'
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
	-	`sha256:c6b11972fd12973831818babf60f1ffc1c4047507943d132dffc612884022858`  
		Last Modified: Mon, 29 Sep 2025 23:34:14 GMT  
		Size: 48.5 MB (48480557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae240525ae2e6d39dc92e86908a0e8d8bc19cb6f221649395d23b16c6fa20951`  
		Last Modified: Wed, 01 Oct 2025 15:49:19 GMT  
		Size: 157.8 MB (157804776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e53d45200af21ed90ffe49f96d110ddb5cbd22c3a610590a821c2720f0b290a`  
		Last Modified: Tue, 30 Sep 2025 00:55:38 GMT  
		Size: 81.1 MB (81145204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cb1369c0267de7c7850ab3f964a8830daea9d6a0d97b2fc18ed61cda8ce9a61`  
		Last Modified: Tue, 30 Sep 2025 00:55:29 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:317951b3a0dcd87a624159e31697edc41a44467ba2f288407f23e596d7ee9efb`  
		Last Modified: Tue, 30 Sep 2025 00:55:29 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:3d4c63d1194f4afc380492a0682e711a5ddb7d1c4aacd210f614716b2e24ed60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7395181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35677f04904a4fda2ef9dfbb18fc0eb29f9f9ad8a5cdb145317e071bb5f0faf5`

```dockerfile
```

-	Layers:
	-	`sha256:34c89b3c5d29462aa86183e8ece9de70007d873bd898c302691f541e1e22a36d`  
		Last Modified: Wed, 01 Oct 2025 15:39:53 GMT  
		Size: 7.4 MB (7378676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40580f4f16a8e441366190b71b693f4e677f5ac2c59fa8633f6b4e51faef10bc`  
		Last Modified: Wed, 01 Oct 2025 15:39:45 GMT  
		Size: 16.5 KB (16505 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:6c5924dc1e5c186d4ee69af3fa75d63a96827256c64c46636883c3bf43a425f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.5 MB (285469482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb5c937fecfd84a0368655385e62f8ae20dfc0bfeff4ed61c0ae5b5b6891510a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1757289600'
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
	-	`sha256:a9331b686701a987bcd276cc69a0f676d471ccda1aa353d2f7fad017f2894cd0`  
		Last Modified: Mon, 08 Sep 2025 21:14:32 GMT  
		Size: 48.4 MB (48359019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adb8e78c8b224c69dcfd6fa4c5371d87c1431dbdcea61588b67945b8343cba3d`  
		Last Modified: Fri, 26 Sep 2025 20:01:15 GMT  
		Size: 156.1 MB (156081195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:970a93479d652e2e0097212ec2dc19354e94c212b095accba44035d0a70dfae3`  
		Last Modified: Fri, 26 Sep 2025 20:01:33 GMT  
		Size: 81.0 MB (81028232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33cbebe6ed944bacef41044c564974c903ffd740da00655cf5c15829e7d31c90`  
		Last Modified: Fri, 26 Sep 2025 18:49:39 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5f70178768e2d40fddc6eab17283e85bf45356256ecc91318005865a7096e18`  
		Last Modified: Fri, 26 Sep 2025 18:49:38 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:261cf7940b40597542d30e5b7e6ec1599349443a7ed198e924e6512ea141b2e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7401109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70ff7cda37cb1f048c9a3b08130045c4f6d0a4d58983479558e9ae241abb312e`

```dockerfile
```

-	Layers:
	-	`sha256:9987a82a43545825c42f972bf10ca88ec00e6df9194d9d3f5f6f1eccae5b734a`  
		Last Modified: Fri, 26 Sep 2025 18:42:18 GMT  
		Size: 7.4 MB (7384463 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18a6e992bec37dea3c86798ed121ae76a65fd52ab5db571e5f747d770807871e`  
		Last Modified: Fri, 26 Sep 2025 18:42:18 GMT  
		Size: 16.6 KB (16646 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:d9816bcdea58763fcecd3b05daa186b6b501258095ee18f83c5f4945e34f924e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.3 MB (297272184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e14e3246d235efd62cc44a57bc6ce9911966e47cd1f75927aae6ad209cb4562a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1757289600'
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
	-	`sha256:64b8116dd43c29a2a4aa3131cb4895af0a7267cc5883e3761556e54c369be9af`  
		Last Modified: Mon, 08 Sep 2025 21:22:08 GMT  
		Size: 52.3 MB (52326822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19b2ca9ff1a3fccb012f6c51a9f097c6995575e5e55d69deb7d54ac91943ca62`  
		Last Modified: Tue, 09 Sep 2025 09:35:24 GMT  
		Size: 158.0 MB (157963479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2422f737257d63b40e7022b8d371108598f213e8923ad64ede63871ef14cd397`  
		Last Modified: Fri, 26 Sep 2025 18:23:18 GMT  
		Size: 87.0 MB (86980844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc298eafe843ec52cde3c920f6be842b18a2e4893a65ee02aa12791c72a9a626`  
		Last Modified: Fri, 26 Sep 2025 18:23:01 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b06b3535b0d9264533c83fe605deb07606a0e889487cc0993da26810afeabf8`  
		Last Modified: Fri, 26 Sep 2025 18:23:03 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:5df2d65f7416bfe66ec7dcd052fefb991e7faac9760af4762eab4383939eafb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7400467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6febafa7bfe76c985cffe744bb5ecab0d4bf5ecd38c97ff4b4a7f1fe194c5405`

```dockerfile
```

-	Layers:
	-	`sha256:1399e7da02796029f77499386031a8a5ad73221b262fa71cbc036b2fad0eef89`  
		Last Modified: Fri, 26 Sep 2025 21:38:59 GMT  
		Size: 7.4 MB (7383902 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2ef3adfbec1fc96bf076d4889660c261f0c1dc454684d4d1ac717917d25db09`  
		Last Modified: Fri, 26 Sep 2025 21:39:00 GMT  
		Size: 16.6 KB (16565 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:5dbb534fc234a004d091d40ad945b65733dff0d693a5553acc29de734565b0b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.1 MB (274121289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:408eb2375c3e6de59426495ee500c21c9b155e1969d59ff2ab35005396ced7bb`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1757289600'
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
	-	`sha256:67e2d91fae4fd9af13e4e364bf8120dcca7856e8273995cc0651acae70b27e8e`  
		Last Modified: Mon, 08 Sep 2025 21:18:01 GMT  
		Size: 47.1 MB (47137539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:884646b634ff5ee33eb640d168094152593cd6db77da73e61da972d291e4950b`  
		Last Modified: Fri, 26 Sep 2025 22:02:57 GMT  
		Size: 147.0 MB (147027032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:220353d08950128c70bf742aed78bd8a4c62edc7a878cb8617f9dff3c89e3e19`  
		Last Modified: Fri, 26 Sep 2025 22:03:04 GMT  
		Size: 80.0 MB (79955671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:989246108dcbf80496dc985a2762109cacbab3e87a4b1a9bac6d6391769b9825`  
		Last Modified: Fri, 26 Sep 2025 20:11:23 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4c71e7f4035d09e145ede554a7b953bcac28e76c5d41b0f89e416ce4454b41a`  
		Last Modified: Fri, 26 Sep 2025 20:11:24 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:f28922cfc2c05ababc8e7a0fd8df9acb03e36a02f45a915bbb65643d53eb914c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7386500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e19d552afde5e7686a8e10c9a25511352d4da1ffdb103a7b1287314a16bd72eb`

```dockerfile
```

-	Layers:
	-	`sha256:40b5c2dcfd44c7c3b47fcd0c5f1842a631e2831a453188af07b4993e9347d2d2`  
		Last Modified: Fri, 26 Sep 2025 21:39:05 GMT  
		Size: 7.4 MB (7369995 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7352fa0807b0e1d3770b86bd782a5f13b7729c29003d040f82d454f15d28edd8`  
		Last Modified: Fri, 26 Sep 2025 21:39:06 GMT  
		Size: 16.5 KB (16505 bytes)  
		MIME: application/vnd.in-toto+json

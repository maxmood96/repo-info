## `clojure:temurin-25-tools-deps-1.12.4.1618-trixie`

```console
$ docker pull clojure@sha256:c26b3208543a1de7d3041b4e4a6025622ff3b7aa14ec937b76f8b7c310425849
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

### `clojure:temurin-25-tools-deps-1.12.4.1618-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:c272d0f5c8f4dc33d11595fe7fc4f7597f33d8b2bc825b35725d60deb092b89d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.4 MB (227448468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97a116cee012e1c04f4336ce3984055b8c4efec5769ef115d1a758d0d3b73687`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Thu, 30 Apr 2026 23:53:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Apr 2026 23:53:41 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 30 Apr 2026 23:53:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Apr 2026 23:53:41 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Thu, 30 Apr 2026 23:53:41 GMT
WORKDIR /tmp
# Thu, 30 Apr 2026 23:53:58 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 30 Apr 2026 23:53:58 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 30 Apr 2026 23:53:58 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 30 Apr 2026 23:53:58 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 30 Apr 2026 23:53:58 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3b32e3bb7338c216b077e95920ae53332d81bd57f4a7393bc324432d5a3f88a2`  
		Last Modified: Wed, 22 Apr 2026 00:16:56 GMT  
		Size: 49.3 MB (49302102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97d7392da51aba5ffbce41ac0432d5c3551bd1265450b818597e3ee9a6b6c1c9`  
		Last Modified: Thu, 30 Apr 2026 23:54:21 GMT  
		Size: 92.6 MB (92574598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31d2a385f0ff4a9f990bf7278f76b0b1f65d46aad0ba8e3681518d38ffa05289`  
		Last Modified: Thu, 30 Apr 2026 23:54:21 GMT  
		Size: 85.6 MB (85570727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2319afa28fe6ac0ca2bc0d32fee4e705bf561e7743cf811a6e5c0de75775c7ec`  
		Last Modified: Thu, 30 Apr 2026 23:54:17 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98c88c53ff0155876d8fd1ee9eeedadafb890032999d6175347888c6c4516361`  
		Last Modified: Thu, 30 Apr 2026 23:54:17 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.4.1618-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:c17119be3e170db50e212fe3e7e11976923de4995398c8817950c2c365f8dfeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7455823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:730deff11b372e84fd75562b8b58ce7cf2b53ee432435adbee2607d6433bca26`

```dockerfile
```

-	Layers:
	-	`sha256:9bb9cd46815abd6699ea05a8a28c81d98265f27f7dbc1bc9ab17d927e7d98d87`  
		Last Modified: Thu, 30 Apr 2026 23:54:18 GMT  
		Size: 7.4 MB (7439410 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6cc7b5ea3d0edf2e60823135c3733965c5d4128aa735f2f09376d22d212910f`  
		Last Modified: Thu, 30 Apr 2026 23:54:17 GMT  
		Size: 16.4 KB (16413 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-1.12.4.1618-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:edb13f4394b624f84678679fec8de1685652558df0ca7d73330e011623033f92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.6 MB (226595835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd4068dfe7516acb032955ebd6054996261aa366b5e6d8f955cddfb42c82ac34`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Fri, 08 May 2026 00:27:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 00:27:45 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 00:27:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 00:27:45 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 00:27:45 GMT
WORKDIR /tmp
# Fri, 08 May 2026 00:28:04 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 00:28:04 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 00:28:04 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 00:28:04 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 00:28:04 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6e7932d5cb5573d1bff4fb8801baad19fc72d2ae741bb046333573653944f5a5`  
		Last Modified: Wed, 22 Apr 2026 00:16:45 GMT  
		Size: 49.7 MB (49669245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05d51095c426ddeb8cc90a9be8db9b5ced6d73b9c0636f8bb160515c4eeff14b`  
		Last Modified: Fri, 08 May 2026 00:28:27 GMT  
		Size: 91.5 MB (91542293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5182c0100a59ccc81716e6d3af8f3267d8518468a54a558e094897b557e7a493`  
		Last Modified: Fri, 08 May 2026 00:28:27 GMT  
		Size: 85.4 MB (85383257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5ce9a09d2a0f3441728568f83d90d40ed0907c6578a96fd1150bdc87842ba21`  
		Last Modified: Fri, 08 May 2026 00:28:23 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc85b78ae4a4a72f6c917d1a76273db2e9cb8d5ded532e9506915402fa6aff82`  
		Last Modified: Fri, 08 May 2026 00:28:23 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.4.1618-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:b4a737881caf265a1ec2e424c29dc46e6f7eab15a44e388f70c65b70c866f59d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7463172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fdb67ecc14a13a98cda0acbcd615def5d736147c49b7084c0143e9e956938c2`

```dockerfile
```

-	Layers:
	-	`sha256:57f7a2a38d3fd14020f61334987373394db8b4c1fec04e2a69469ad3c3e1186b`  
		Last Modified: Fri, 08 May 2026 00:28:24 GMT  
		Size: 7.4 MB (7446461 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f960f1852ae0b761cb6bdd55ab752ed0617465938c11df8f8d64feb554c35d90`  
		Last Modified: Fri, 08 May 2026 00:28:23 GMT  
		Size: 16.7 KB (16711 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-1.12.4.1618-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:fff126743735f3e030ef44a0f71e5b9aa1bbe08ad63c72b9c6673103fcb8cf54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.0 MB (236024336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12dc45acc995349f7e03946d16720941c7493d10370da37dad8cdc296cf4ad51`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1776729600'
# Fri, 08 May 2026 01:44:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 01:44:02 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 01:44:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 01:44:02 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 01:44:03 GMT
WORKDIR /tmp
# Fri, 08 May 2026 01:48:41 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 01:48:41 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 01:48:42 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 01:48:42 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 01:48:42 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0fab4f6170940889900b2327e1b3c62dace993eab8074ca7d33d1ffeef137c08`  
		Last Modified: Wed, 22 Apr 2026 00:18:18 GMT  
		Size: 53.1 MB (53122984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10c0840b059b135fa7f7f221d2f316e4eeea1c12b50461d42b38e0a6be805d85`  
		Last Modified: Fri, 08 May 2026 01:45:19 GMT  
		Size: 91.9 MB (91914028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5397dec3296fc6bd3e45ec89950702ed3adff883fe89eca573ec0a1351ca897`  
		Last Modified: Fri, 08 May 2026 01:49:20 GMT  
		Size: 91.0 MB (90986286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:083894e9db61acf8567e12b8191f0d09cec27cffaf5cdedc8302a2ecff617efb`  
		Last Modified: Fri, 08 May 2026 01:49:18 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfc77b78d53e140ca0059c72e323c9e223b653457856486c6a6209c12b20e1e4`  
		Last Modified: Fri, 08 May 2026 01:49:18 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.4.1618-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:4d91d784868fa0d3f2c49db1af756a8febbf3c0707dcb66c86ebf74bf09b3aab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7443782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb75ef0c86f79d018d5f6bb8aac6bdba6c64482701861457fc0df12e8f7e788d`

```dockerfile
```

-	Layers:
	-	`sha256:7d1757647ff1af93f908ce51cc8071822ab2d781b4352ab198f67880a165e778`  
		Last Modified: Fri, 08 May 2026 01:49:18 GMT  
		Size: 7.4 MB (7427155 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53c7947180faf1944b751bb423c2c9f7abbdc709448701ba276990fd17461662`  
		Last Modified: Fri, 08 May 2026 01:49:17 GMT  
		Size: 16.6 KB (16627 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-1.12.4.1618-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:9a0007e2a153006241a654c4b8ee0c8f88163625680fc7f26f1ef3d13e047ac8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.3 MB (223274071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:934285164367c88eaeb9b8e69b6c785cd8cfe3f852f960064309a5f872e4146c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1776729600'
# Fri, 01 May 2026 01:11:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 May 2026 01:11:16 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 01 May 2026 01:11:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 May 2026 01:11:16 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 01 May 2026 01:11:16 GMT
WORKDIR /tmp
# Fri, 01 May 2026 01:32:29 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 01 May 2026 01:32:29 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 01 May 2026 01:32:29 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 01 May 2026 01:32:29 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 01 May 2026 01:32:29 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6e518626ae0de2d990c7c66185d308a25cb3affebb6204543438f56fd9f94992`  
		Last Modified: Wed, 22 Apr 2026 02:29:17 GMT  
		Size: 47.8 MB (47798217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af697d12e7ce2f4ea84af1fb9a0a596fbf93eb7670e91abadfbefd74c762bc67`  
		Last Modified: Fri, 01 May 2026 01:16:52 GMT  
		Size: 91.0 MB (91014936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:729740652b4cdbc2e6ee0c940fe6fe37b8ec7989bf2496b18e671869ad050db5`  
		Last Modified: Fri, 01 May 2026 01:36:54 GMT  
		Size: 84.5 MB (84459880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a58db505e492a7bb0d48cca60146b61495e9ead3380a725f193a3a4d17d3f432`  
		Last Modified: Fri, 01 May 2026 01:36:35 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07e1f66b7ede5991fa02e70eae90c25e30431446b587ea7f4e3275b0607e8f64`  
		Last Modified: Fri, 01 May 2026 01:36:35 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.4.1618-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:504a26518932b2148c1bc15b84d3c62114c456887eb6644d891dd497910fee9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7425823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ddfd037d939382667b089d2ba0c82e0bf2e92fc617f4e59ed47dce6c6e1c863`

```dockerfile
```

-	Layers:
	-	`sha256:d8542829608a38f8b3b2340b5acafd7a072fba248a0fb37772a6874d018f47ea`  
		Last Modified: Fri, 01 May 2026 01:36:37 GMT  
		Size: 7.4 MB (7409348 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58d28545eb03c413f36a2e0b34d5ea5c6809bcd976e29717a20b1c33ad9a48e9`  
		Last Modified: Fri, 01 May 2026 01:36:35 GMT  
		Size: 16.5 KB (16475 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-1.12.4.1618-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:9d41f1eeaa0b0b5147dfff3a6cae378d7f80071dc0efce55cc82db999c666cdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.3 MB (224338809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c38a3767196f9bb8f34e54f6c54efe93be93c9250baa8818e89139044b7af3ea`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1776729600'
# Thu, 30 Apr 2026 23:52:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Apr 2026 23:52:02 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 30 Apr 2026 23:52:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Apr 2026 23:52:02 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Thu, 30 Apr 2026 23:52:02 GMT
WORKDIR /tmp
# Thu, 30 Apr 2026 23:52:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 30 Apr 2026 23:52:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 30 Apr 2026 23:52:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 30 Apr 2026 23:52:26 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 30 Apr 2026 23:52:26 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:943402c24d6e7299016c00f751297dfb5fc1821547fdd1d9c56a206079784185`  
		Last Modified: Wed, 22 Apr 2026 00:17:09 GMT  
		Size: 49.4 MB (49372106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc9a52fd9c513687d75c7681b6b507b51cbb775a31cb9520450f2655339d9667`  
		Last Modified: Thu, 30 Apr 2026 23:52:57 GMT  
		Size: 88.4 MB (88420322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a7fe5abdf2b316901c9363815e16a047c35304a2395c2051e905a8b39185899`  
		Last Modified: Thu, 30 Apr 2026 23:52:57 GMT  
		Size: 86.5 MB (86545343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d635664bf9270565247177e91cfd4adc5d53656740b579aa79012e55d6443a5`  
		Last Modified: Thu, 30 Apr 2026 23:52:55 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51c6a6a0a950ad060be0a0e1bd25ebf6e3e37ba69f8336bbd4b3367106a4acac`  
		Last Modified: Thu, 30 Apr 2026 23:52:54 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.4.1618-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:ff7c6debdf8377e6a1d7d6634efd5c9d612cb24fa1ce29dedeb0448885291d98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7436309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fba5c5bff5a7e12e924ee401f2f764d5afc3d657b7f2091ba338a054c8ab45c8`

```dockerfile
```

-	Layers:
	-	`sha256:ea509f8070156c16aed92f47b2752e918f7c0cf609d05fd2b96c005009ba9c76`  
		Last Modified: Thu, 30 Apr 2026 23:52:55 GMT  
		Size: 7.4 MB (7419894 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f595bb38554e5f7425cdf229d48c5e480e0c9057b9a764bdf9b523bc9ea049b4`  
		Last Modified: Thu, 30 Apr 2026 23:52:55 GMT  
		Size: 16.4 KB (16415 bytes)  
		MIME: application/vnd.in-toto+json

## `clojure:tools-deps-trixie`

```console
$ docker pull clojure@sha256:c48b37171121d8d8bc8da4c456a48786864514f26379b89d13d9d6ac3b1f0a18
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

### `clojure:tools-deps-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:b380d17b7b1ebeb5630eba3aafe4950ccb0e729dc170284159ceb55b9a0d3fb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.4 MB (227448266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:610a1426e61daa1a57126393b8b0a4a1acd92182953f8540d4e2c8a31c3b9575`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Fri, 08 May 2026 00:28:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 00:28:28 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 00:28:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 00:28:28 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 00:28:28 GMT
WORKDIR /tmp
# Fri, 08 May 2026 00:28:45 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 00:28:45 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 00:28:45 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 00:28:45 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 00:28:45 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3b32e3bb7338c216b077e95920ae53332d81bd57f4a7393bc324432d5a3f88a2`  
		Last Modified: Wed, 22 Apr 2026 00:16:56 GMT  
		Size: 49.3 MB (49302102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1abca5e026008f41ea35ab40ee9bd29db5a7d1a62b96eca049162d1ccc7cfc12`  
		Last Modified: Fri, 08 May 2026 00:29:06 GMT  
		Size: 92.6 MB (92574588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96b684cf0b16d11ba3662adab50e9c4a115713515ac4bbe916e0ecce6d8a5f26`  
		Last Modified: Fri, 08 May 2026 00:29:15 GMT  
		Size: 85.6 MB (85570537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4853ecd57fd661916097adcaa402c08ff45f22d0de3e0dbb641b40328b4cb559`  
		Last Modified: Fri, 08 May 2026 00:29:04 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60de305f126f3f1d2e4bebf79160add0ad185a64f3e06af63d4c185c828df205`  
		Last Modified: Fri, 08 May 2026 00:29:04 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:873c9431b287c763a4f9bb4105a60a0a6f782f541158da6af1fbec4e54679b0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7455979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:222431c44d5fc4b393cd56a03d9337d61d6fee430b37dbba7ac68f90b1248275`

```dockerfile
```

-	Layers:
	-	`sha256:82577dbe7b5b08a7cf4ef54ea8158466d22b36258ab812c226c6f56b20d65ea2`  
		Last Modified: Fri, 08 May 2026 00:29:04 GMT  
		Size: 7.4 MB (7439410 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c8fe292d29c74d8335373db0ab1eb3e9af034450ea7fef69a62c5cc7352f79e7`  
		Last Modified: Fri, 08 May 2026 00:29:04 GMT  
		Size: 16.6 KB (16569 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-trixie` - linux; arm64 variant v8

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

### `clojure:tools-deps-trixie` - unknown; unknown

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

### `clojure:tools-deps-trixie` - linux; ppc64le

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

### `clojure:tools-deps-trixie` - unknown; unknown

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

### `clojure:tools-deps-trixie` - linux; riscv64

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

### `clojure:tools-deps-trixie` - unknown; unknown

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

### `clojure:tools-deps-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:c6be880628444d003749754d3af8232ae3a127113642da6f3377150adab02e24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.3 MB (224338161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3cd741cce8d76b802485742ba749b107c955802ca57fc940d9c112407627d47`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1776729600'
# Thu, 30 Apr 2026 23:50:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Apr 2026 23:50:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 30 Apr 2026 23:50:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Apr 2026 23:50:51 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Thu, 30 Apr 2026 23:50:51 GMT
WORKDIR /tmp
# Fri, 08 May 2026 00:41:25 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 00:41:25 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 00:41:25 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 00:41:25 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 00:41:25 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:943402c24d6e7299016c00f751297dfb5fc1821547fdd1d9c56a206079784185`  
		Last Modified: Wed, 22 Apr 2026 00:17:09 GMT  
		Size: 49.4 MB (49372106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72ee46c033b5990060b9acaa5985a11a008290bfbbb27b32d546e2487a9a5e65`  
		Last Modified: Thu, 30 Apr 2026 23:51:37 GMT  
		Size: 88.4 MB (88420341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a183315f7c152cbf8a8c812ca33f52a9ccb590356ed80605e4dae5f775bf25ff`  
		Last Modified: Fri, 08 May 2026 00:41:51 GMT  
		Size: 86.5 MB (86544674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3298964f87f321a9af9060e0f28310634b10aa249d37195c48d492ae56e3f2c`  
		Last Modified: Fri, 08 May 2026 00:41:50 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8632cb8eebb58c76d06a6a5663f91140da2f8447549e678837fcc85e86f047b`  
		Last Modified: Fri, 08 May 2026 00:41:50 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:5c12e9c4d31798c091f579734ff1feef79ee866c7d4865cc6e3303ea190bb40f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7436462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d73b6d8f0715af9247811a90fa376cd5ffbd17e72792467c947c95a379ea89b2`

```dockerfile
```

-	Layers:
	-	`sha256:f2be4a77c6055a5d9aa2ce25f259ebad551cadfa134267d4fd8c282d3ab6019b`  
		Last Modified: Fri, 08 May 2026 00:41:50 GMT  
		Size: 7.4 MB (7419894 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2fa8db1b57950dccf834a6926e70b71decab848b0f3de2fc7abdf24220cdf420`  
		Last Modified: Fri, 08 May 2026 00:41:50 GMT  
		Size: 16.6 KB (16568 bytes)  
		MIME: application/vnd.in-toto+json

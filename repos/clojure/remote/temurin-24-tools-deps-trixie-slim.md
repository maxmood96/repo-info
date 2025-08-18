## `clojure:temurin-24-tools-deps-trixie-slim`

```console
$ docker pull clojure@sha256:5142b74a0097aa118707a97c8588c74402e0cba7d5d63d8df1eed32e52e08916
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

### `clojure:temurin-24-tools-deps-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:6762865d56cb989947842f8844e5940131d2330363854d77e553b2c2258cfdc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.6 MB (191638931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e565d486f753e8d362dca7a57943ad8945bf79e2c69d1e66f9ab006253d3e41`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1754870400'
# Sat, 16 Aug 2025 23:31:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Aug 2025 23:31:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Aug 2025 23:31:29 GMT
ENV CLOJURE_VERSION=1.12.1.1561
# Sat, 16 Aug 2025 23:31:29 GMT
WORKDIR /tmp
# Sat, 16 Aug 2025 23:31:29 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b0328626c508af54c3eaf00cfb67e85d5215c6447b15c8ecc70fbe29ca95d64e *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 16 Aug 2025 23:31:29 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:396b1da7636e2dcd10565cb4f2f952cbb4a8a38b58d3b86a2cacb172fb70117c`  
		Last Modified: Tue, 12 Aug 2025 20:45:08 GMT  
		Size: 29.8 MB (29773285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b96315b1b178f9c08e69bdeaec55f0824d724c4ae6c4591e9a80e87ee2f3b511`  
		Last Modified: Mon, 18 Aug 2025 20:13:09 GMT  
		Size: 90.0 MB (89975262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b6ad55c67afdb63dcd7ce8f4042ba0b927281f2ab195a5c0ec9baf68dbfca25`  
		Last Modified: Mon, 18 Aug 2025 16:53:23 GMT  
		Size: 71.9 MB (71889342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98e3d25b96957e3a20399e4e51ead2d10b03c4ff6e1a415b5147491442368384`  
		Last Modified: Mon, 18 Aug 2025 16:53:13 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92c6664c6f41922bf76dfaf370781e15bce559d00b27ab37a553161b3a535314`  
		Last Modified: Mon, 18 Aug 2025 16:52:33 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:6174c0dde8049d92ea5e0c63a03af1d8092e4a5a8f5149791f9a5b893a59f1b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5221733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7309ce7ef19bceb1e3dcbc3e19de65eae13bdb8b6c70760781fc21ec51d61f0d`

```dockerfile
```

-	Layers:
	-	`sha256:1f217fed0396198f1f84ae897713b03fc4c8e091ba578530cd25df6b868662db`  
		Last Modified: Mon, 18 Aug 2025 18:43:57 GMT  
		Size: 5.2 MB (5205885 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d0ec5eb08578a2801bed7751df75d50d714c07c57d63187a7092526be54d5fd`  
		Last Modified: Mon, 18 Aug 2025 18:43:58 GMT  
		Size: 15.8 KB (15848 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:d4726e0d55c361a8a0d00d24d1b5380be5226329f2b5d77caa1bdfb2bae5924e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.9 MB (190936334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8d63c16721401fda2cc3d5d642eee51a4a658f5b6f7292ad0bb2eb49f32faba`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1754870400'
# Sat, 16 Aug 2025 23:31:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Aug 2025 23:31:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Aug 2025 23:31:29 GMT
ENV CLOJURE_VERSION=1.12.1.1561
# Sat, 16 Aug 2025 23:31:29 GMT
WORKDIR /tmp
# Sat, 16 Aug 2025 23:31:29 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b0328626c508af54c3eaf00cfb67e85d5215c6447b15c8ecc70fbe29ca95d64e *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 16 Aug 2025 23:31:29 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:9a6263cdeaa5d408640880103ee36920ef814974ca8e2674412ad6460e8968c9`  
		Last Modified: Tue, 12 Aug 2025 22:12:42 GMT  
		Size: 30.1 MB (30136044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebe54333b06ad8dc6a1c19356b2654e06d357097398ccfe7bcc23b46b25aca1b`  
		Last Modified: Mon, 18 Aug 2025 17:25:14 GMT  
		Size: 89.1 MB (89092501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4db14d9b00d94eefb7893f5a19421150739f6b029f946293576fc90d2637aa42`  
		Last Modified: Mon, 18 Aug 2025 17:25:13 GMT  
		Size: 71.7 MB (71706745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5130ac70dbaee1c645c8d38f0e8fc521d95573ada5fda8937fef9ee89638bf75`  
		Last Modified: Mon, 18 Aug 2025 17:25:04 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f23318e5af86a6213dfa5d9a54698a2392807919b8d94d2988c4fbe4ba026791`  
		Last Modified: Mon, 18 Aug 2025 17:25:05 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a1c1a4bbcb1b5f446cdfa8ea9b36240cfe3bc54e9636cdcb7306706914720a5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5227617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8f888093b55c83a5aca4bf8f78ba188fc0cbc7c9942496edaf4672f29542a46`

```dockerfile
```

-	Layers:
	-	`sha256:6a03633810835ae2b87e495a865edb6e62bfedfe6592016c05cab81c364de218`  
		Last Modified: Mon, 18 Aug 2025 18:44:03 GMT  
		Size: 5.2 MB (5211651 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f750397b8c4c419ee4ba64dc0b0ed8256e12062920a155cb741e819f50157721`  
		Last Modified: Mon, 18 Aug 2025 18:44:04 GMT  
		Size: 16.0 KB (15966 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:07b2f06a70a42905c946cb6958a2df22f955d00af0a950c95f1cc32a020f07d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.8 MB (200803791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ca3f625c8f4915b508cb9258d43e42b865df21b27cfe9d3775b103f2b12ad65`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1754870400'
# Sat, 16 Aug 2025 23:31:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Aug 2025 23:31:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Aug 2025 23:31:29 GMT
ENV CLOJURE_VERSION=1.12.1.1561
# Sat, 16 Aug 2025 23:31:29 GMT
WORKDIR /tmp
# Sat, 16 Aug 2025 23:31:29 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b0328626c508af54c3eaf00cfb67e85d5215c6447b15c8ecc70fbe29ca95d64e *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 16 Aug 2025 23:31:29 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:52a4daa8724e9e1632306e15fe478aa26ff0ebcb7ba924cb168e9b6738c239d5`  
		Last Modified: Wed, 13 Aug 2025 01:42:36 GMT  
		Size: 33.6 MB (33594213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:344e68d3b82d646b17664e62a5168a46a359609aeb0118f6b14ccf55dbdbe212`  
		Last Modified: Mon, 18 Aug 2025 17:41:28 GMT  
		Size: 89.9 MB (89918237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:959181a9738e1b91b1b2bcb37af75b497e68825affad2df3b3c37c81fc619a70`  
		Last Modified: Mon, 18 Aug 2025 17:41:28 GMT  
		Size: 77.3 MB (77290297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b96e24da669fc2e3faa77a6fdbfd91843e863e0ee4af48d24b5a56e273aeb64f`  
		Last Modified: Mon, 18 Aug 2025 17:51:58 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d738df5078ad7d302705e1989ce9757b89b51f8913ad3422d3c855deeaf6dd98`  
		Last Modified: Mon, 18 Aug 2025 17:51:49 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:6fbe1bfe9579bfda72dfba40cb8f96b2011f00072cd13192ca3a5208b6c36ec8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5227450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db91518528770e4b976409d0a65e02ddd0a7555660e6b44f2192ae772bb58828`

```dockerfile
```

-	Layers:
	-	`sha256:9ef6e68ce4a8e4cd72e7a9f19d289049dff79653bef2dfe83b6f2d58fd4e1872`  
		Last Modified: Mon, 18 Aug 2025 18:44:11 GMT  
		Size: 5.2 MB (5211554 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65734fd225161e6ddad6ff8746c5423431c51f52637b4b1a31db7571e030ec23`  
		Last Modified: Mon, 18 Aug 2025 18:44:11 GMT  
		Size: 15.9 KB (15896 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:300eea5da186f420dd86cbaeb411f0b7b086729952dd12cdcf6de1a0596ad024
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.7 MB (186674475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f5b9f1d685aaef323b9e695f02014a4648e7854f5bb7f2b596dd10c3bbd3c91`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1754870400'
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
	-	`sha256:a37386b9234ad75f65b5aa72f3d919ff0eb3bb18978566fa959d6e357480594c`  
		Last Modified: Wed, 13 Aug 2025 04:01:43 GMT  
		Size: 28.3 MB (28271623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97125372afb3e2f47113a36e62b460f48c50f45d3384089379e7fcbef7e6354a`  
		Last Modified: Fri, 15 Aug 2025 08:12:50 GMT  
		Size: 87.7 MB (87670395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:121c6abdb7d0081be9168deb88d9e2c792ad68fadeb8d691d241c3a27335db75`  
		Last Modified: Fri, 15 Aug 2025 08:26:36 GMT  
		Size: 70.7 MB (70731415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae9e2c85cb2282341472b751b49e75057802ca88a97552270796bedc66e6c4cf`  
		Last Modified: Fri, 15 Aug 2025 08:26:32 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:811a0aa8afbe735914053a379fd78204dc9c5067d02f2cfc22eca66c9a5d6757`  
		Last Modified: Fri, 15 Aug 2025 08:26:31 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:5323313d2acd89501cd0a94755ee75b2d186be3ad6f12841b95ed3a7fe810875
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5211213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42331ed48e9ab896e01d5aabe7195c742b571c207ad61f0a2365f869b40e6c97`

```dockerfile
```

-	Layers:
	-	`sha256:448cca53ba06a8bf09e13492b740bd434f0f31ae8287feee019daf5d63b2e51e`  
		Last Modified: Fri, 15 Aug 2025 09:37:47 GMT  
		Size: 5.2 MB (5195317 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5f5bfdf001966cd532c7c6138400dccfa8d61c518e8eee08639cba9cf4752d2`  
		Last Modified: Fri, 15 Aug 2025 09:37:48 GMT  
		Size: 15.9 KB (15896 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:473a81e5f15c0a473c1f38d155cb9866db203445c468d735301097f73cc9cb0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.9 MB (187911251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:902ddab8429102f485e68fe15d2b65c3c471ad5a24d6b3b33564cb255a25bc3a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1754870400'
# Sat, 16 Aug 2025 23:31:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Aug 2025 23:31:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Aug 2025 23:31:29 GMT
ENV CLOJURE_VERSION=1.12.1.1561
# Sat, 16 Aug 2025 23:31:29 GMT
WORKDIR /tmp
# Sat, 16 Aug 2025 23:31:29 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b0328626c508af54c3eaf00cfb67e85d5215c6447b15c8ecc70fbe29ca95d64e *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 16 Aug 2025 23:31:29 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:bfe4d60a27c9392ab729f16b50a763cda36622d744066c3cf029a072133f2907`  
		Last Modified: Tue, 12 Aug 2025 20:59:52 GMT  
		Size: 29.8 MB (29833057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec43252ef36a8b912f0b9161e21f8c05ad6c75f47c25da09877a4661719d555d`  
		Last Modified: Mon, 18 Aug 2025 18:26:18 GMT  
		Size: 85.2 MB (85226400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:276d9ea90fb039a57d302e922d0eeedefbc6190a95927653e3c07861b7b04e3e`  
		Last Modified: Mon, 18 Aug 2025 18:26:14 GMT  
		Size: 72.9 MB (72850752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1289937791073124aa0362d7ab68ac616e08e046a8b1e36c5723b9799c496105`  
		Last Modified: Mon, 18 Aug 2025 18:26:05 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15040d2cd667056dde49804eb29b00b83bd3addfd6db2144f3ef9c931bfa49a6`  
		Last Modified: Mon, 18 Aug 2025 18:26:05 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:9d29e07871ddc620c863c662462f92127054b8df9ebb9ffeb7ab231fe3701b9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5220205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f6a3f3500b9c9d77a823dd38882020b92770b2c1d4994c6796407c9a6fa7a27`

```dockerfile
```

-	Layers:
	-	`sha256:9cc37780e0e229ae0ffc24502786b74100d9f4fd8cfa4cc12df90a884dc81a3e`  
		Last Modified: Mon, 18 Aug 2025 21:37:01 GMT  
		Size: 5.2 MB (5204357 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e7fd77cc7b08c1f1c6639b3f39024b8bb7fe10e66f8304cf256c5d7c5145ef5`  
		Last Modified: Mon, 18 Aug 2025 21:37:03 GMT  
		Size: 15.8 KB (15848 bytes)  
		MIME: application/vnd.in-toto+json

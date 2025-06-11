## `clojure:temurin-24-tools-deps-trixie-slim`

```console
$ docker pull clojure@sha256:bed9b2689af53acc85a992cf964ba9ef07dfaafafa7de187d5dc52b4f5c45433
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
$ docker pull clojure@sha256:e2eb814b317371ca7640fe21e371a76f67ae3c45c27919dfb3e102c897b7a88c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.4 MB (191431400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2a881b2771b448defe593bd269a660e6c6e0db78376836eb346d821bbb0ad69`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1749513600'
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
	-	`sha256:6f052c0ff895d860a8f6983dcf5207c5e8ff5949529101bf68c1e92e9c8baf36`  
		Last Modified: Tue, 10 Jun 2025 22:47:31 GMT  
		Size: 29.8 MB (29756816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05797adc8c500e1e24c2b27b5d7a490bd7b6b7ee01c3ea01546d2188ff0f76ca`  
		Last Modified: Tue, 10 Jun 2025 23:53:36 GMT  
		Size: 90.0 MB (89952003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57abe2830dfb91c22ac3389b50a0a5c5644e6c1ac7984b82d7fba640f78e372d`  
		Last Modified: Tue, 10 Jun 2025 23:53:35 GMT  
		Size: 71.7 MB (71721539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a7ac8614f1452dc4def8895f9ee9d727ae0fad6e94c893ea64764a2199e5f12`  
		Last Modified: Tue, 10 Jun 2025 23:53:19 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65f4cbd2551f72abb213a8e28fa2054ea0ca0440dfea5d0e3d8b16b859069748`  
		Last Modified: Tue, 10 Jun 2025 23:53:20 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:500f3e7add9ff169ba29f476316b35aa237d9b400c48929e8d415662bc299d85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5219292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:583e68beaf46ffe6097bc421e7134deacd28652b2a3206ab2ca9102ccb09b9ab`

```dockerfile
```

-	Layers:
	-	`sha256:f97c6dd68816e2fbacf7504fff95632421aae82a9b19cba9054166d0962a4413`  
		Last Modified: Wed, 11 Jun 2025 03:41:06 GMT  
		Size: 5.2 MB (5203444 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5680a4fa1a98931319aae36ffc04b5e54af886ac541d03fd1b8c27acd4ec90d1`  
		Last Modified: Wed, 11 Jun 2025 03:41:07 GMT  
		Size: 15.8 KB (15848 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:dc32a5ddb6176e4f1628fc0a37e732216b79a939c927ff2b06fd70459bceb35a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.9 MB (190880649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f7aca93ef618f3f1423d8278b601d14e9a1d7e617d8c9e80d3bc1070ab3ed4a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1749513600'
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
	-	`sha256:c3306e90503bf56d5d575fca0323e4953fc66cffec788094159d11570a81151f`  
		Last Modified: Tue, 10 Jun 2025 22:53:04 GMT  
		Size: 30.1 MB (30121041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1c8750a27004b373ccbbac455cc03e609a08cb23334c213f27833d57177f0b1`  
		Last Modified: Wed, 11 Jun 2025 08:46:33 GMT  
		Size: 89.1 MB (89091271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95773a5d791f45e56ddbe3d339778716df7043ebe37a7f362f089c8fa67ac34e`  
		Last Modified: Wed, 11 Jun 2025 08:50:33 GMT  
		Size: 71.7 MB (71667296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f0fe9886938ab5bdde821ea824f9986c0936d337bbbb5fb1fb36f287aac79f2`  
		Last Modified: Wed, 11 Jun 2025 08:50:24 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ad927961fe4b4b0400629b38b59bb301ce543da6dbb154b7d393deaf2d3b942`  
		Last Modified: Wed, 11 Jun 2025 08:50:24 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:565bb55b0e067eaedec07db58d292a6ca6247fb4082aed7a719527b53b0c1b8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5225176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:701667aa75c57901c118c33a60e818796fe6afa830cc3174df3849c5c014914e`

```dockerfile
```

-	Layers:
	-	`sha256:f422e820354549a7363e4f2a0ba22c3a294be5b5d4aad2e1e6f19f6bb101b812`  
		Last Modified: Wed, 11 Jun 2025 09:42:19 GMT  
		Size: 5.2 MB (5209210 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:07a5060b37762fc8a783de71eca89fbf9d60a21fb68a2f5396313162a8aadc1a`  
		Last Modified: Wed, 11 Jun 2025 09:42:20 GMT  
		Size: 16.0 KB (15966 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:d529c14396e7ee931c61b1be161a9a3fdbdc0bb3c271685a775ae46e867df864
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.7 MB (200738286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:894f653d26753623012041f3d2ffe5ebc025003f2fa1c08a5308ffbed1f923c1`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1749513600'
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
	-	`sha256:9851a8240d92395a99e35175026ad70b4eb50fb4e03132b209af1bf02a1fa307`  
		Last Modified: Wed, 11 Jun 2025 00:37:24 GMT  
		Size: 33.6 MB (33580925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4791b561440f182ebb1a5541ddb101a1fc65ce7da877f274b1ba592b8cff863`  
		Last Modified: Wed, 11 Jun 2025 08:57:36 GMT  
		Size: 89.9 MB (89920271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c299ccdd645d9db70677eb32617186cfac70941ca67da8fdb94528bb652b4a37`  
		Last Modified: Wed, 11 Jun 2025 09:03:45 GMT  
		Size: 77.2 MB (77236050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fac078a92e24265ea7bd11283c2f03773f30fc8f535a6c4031b3d52a5b199ff`  
		Last Modified: Wed, 11 Jun 2025 09:03:37 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:035a7b5342afbdd7e965aea0e4f78175a509bf814f96fd255b099312b465030b`  
		Last Modified: Wed, 11 Jun 2025 09:03:37 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a2f941bccf38b19c68e704e88f19dc42c21581894ec8480f94cb43dfcbf27128
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5225009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2b5dae5427f8157ec611f6fb13b493df7fcb2a68040631c2c9c7dfef354fb40`

```dockerfile
```

-	Layers:
	-	`sha256:1eaa5699b65cf6319f4d46b39754520425dd6572eec2cd546a92fe950ca3d2aa`  
		Last Modified: Wed, 11 Jun 2025 09:42:25 GMT  
		Size: 5.2 MB (5209113 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16c57a54447ee6286a335a22cca855484131db787a468a99a0580c689837d75e`  
		Last Modified: Wed, 11 Jun 2025 09:42:26 GMT  
		Size: 15.9 KB (15896 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:021eda093c7a9646aaa682533a9899a29f848856f9f6cf29a4f4986229f5ca71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.6 MB (186584067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f580f1a754896a92a9f24c9f72831c8e8ec391f23a5792c6e53770580774d727`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1749513600'
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
	-	`sha256:3a4ce3b49438d6e971d6a25501e5ee98899a309dea36cc03fae31602fe4551a7`  
		Last Modified: Tue, 10 Jun 2025 22:57:56 GMT  
		Size: 28.2 MB (28247070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a09b883acc3f8428b9c4a6efa04367b7b31096d2a081942d7e9869aa32ecf132`  
		Last Modified: Wed, 11 Jun 2025 01:20:38 GMT  
		Size: 87.6 MB (87622163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34566a4f14852d44d5c4ff12e84806122c5baa423855e43d829d61b4283092f7`  
		Last Modified: Wed, 11 Jun 2025 01:34:37 GMT  
		Size: 70.7 MB (70713789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7285f877b22136cd22ceb8bb9f24778c3e3273acbed27756a6fd67061f1d1c22`  
		Last Modified: Wed, 11 Jun 2025 01:34:31 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cc44e68107ff1a0a07955ee2f5d1903f15201f8961f22e71b01fda6542eea74`  
		Last Modified: Wed, 11 Jun 2025 01:34:31 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:7d7e6ab2c8b30615c5a5a26caa5c85535eca5933f717482e715569835e4c9ffd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5208800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0176b88efff133eed6f948bab40bee34ed737e6f5c1583ae0085495ed261c85`

```dockerfile
```

-	Layers:
	-	`sha256:f09bdca696eb7be98a466f5eb883beed65aec0e6d3e9f2312845e2e8d10f9f6a`  
		Last Modified: Wed, 11 Jun 2025 03:41:19 GMT  
		Size: 5.2 MB (5192905 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ccc8595ac21638fd9a1167e839da7fa4473353361bcb993e319996519ed37db1`  
		Last Modified: Wed, 11 Jun 2025 03:41:20 GMT  
		Size: 15.9 KB (15895 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:117b87a4d3547b08cccbfa8456d7fc8c7a3aca9402192383aae0d298b53c9604
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.9 MB (187869828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:525e2b40c3a6b6ab0b18c0771ac46fa10814cc82ba1575187a3205bd6c68b9b7`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1749513600'
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
	-	`sha256:c274825e96bcfbbdcdc116bb72e2d5d06d51048380b2fb22f400e6f9627616b6`  
		Last Modified: Wed, 11 Jun 2025 00:37:39 GMT  
		Size: 29.8 MB (29831871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7c7cc589757c99b9a6c70ea25d07fec2debb77f0d316713df01008d5f09355e`  
		Last Modified: Wed, 11 Jun 2025 12:07:25 GMT  
		Size: 85.2 MB (85216750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:890f3a91817cce5569e79e9e2bdeff18557149fa8a501dc5e1f406583c9a8d1b`  
		Last Modified: Wed, 11 Jun 2025 06:04:57 GMT  
		Size: 72.8 MB (72820167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5b01cabe3906946aa67d8a1e1664d4701e101639eec3837ccf49c054e5e9ba3`  
		Last Modified: Wed, 11 Jun 2025 12:20:28 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88f5db77608d97506ff67d30c670b75671eb3c6a88997ccbcf0011e6a6beaa8b`  
		Last Modified: Wed, 11 Jun 2025 12:20:31 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:2761159ef90c3ae3f10182754df0d38af393a8768d9681a9423f4b1945ce74a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5217764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1381f9085b892f8ac4b2ab8f6a2f5da2a2871504020917092e0d1864fa5cadda`

```dockerfile
```

-	Layers:
	-	`sha256:76484aee3d769676c283de4ebba7b1aee3bc434092aef4a77d7b579178f953d6`  
		Last Modified: Wed, 11 Jun 2025 06:39:51 GMT  
		Size: 5.2 MB (5201916 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa2fa61afa47e5ad4194624d0a073be88dc01f6dc4f6ea2099191cefb7b80c77`  
		Last Modified: Wed, 11 Jun 2025 06:39:52 GMT  
		Size: 15.8 KB (15848 bytes)  
		MIME: application/vnd.in-toto+json

## `clojure:temurin-17-tools-deps-1.12.4.1618-bookworm-slim`

```console
$ docker pull clojure@sha256:fa79695f3b152c4d159104ac31176571d30669a4bf4057f5bc6c7c01b85f51d0
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

### `clojure:temurin-17-tools-deps-1.12.4.1618-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:938bf396f513c2a3ce6685f7b8a44a0b307222b4739bdbcf92bd1d7cf754f46f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.8 MB (243841883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aeda5801f1de1363d9eb5c9857d511ae939b13c2855c8a44407843fbe58cb153`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1776729600'
# Fri, 08 May 2026 00:07:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 00:07:48 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 00:07:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 00:07:48 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 00:07:48 GMT
WORKDIR /tmp
# Fri, 08 May 2026 00:08:02 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 00:08:02 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 00:08:02 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 00:08:02 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 00:08:02 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ff86ea2e5edce334d19a34fbc65d1a511aa1fc823dba1110422f991aa56b44d4`  
		Last Modified: Wed, 22 Apr 2026 00:16:25 GMT  
		Size: 28.2 MB (28236252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24067c34c83f7c3d4a8688ad4c1dcf92b715cce45f15af3d62756db51bdaaae1`  
		Last Modified: Fri, 08 May 2026 00:08:23 GMT  
		Size: 145.9 MB (145905487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a43d11ce742f21843485f05eaaabd71983ab60739a70b05e4be4faa038f5bf6`  
		Last Modified: Fri, 08 May 2026 00:08:31 GMT  
		Size: 69.7 MB (69699105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f12860c7888657e921b1c1d01d588774ad7bf8590d16d5eb3c596897329a4de`  
		Last Modified: Fri, 08 May 2026 00:08:19 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dff34110ebfb02ef3ae3e4135434be5d5d071c55b125c85975d42b054798bbf1`  
		Last Modified: Fri, 08 May 2026 00:08:19 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1618-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:6b3f6ff86942fa9791fa879fd30b3350ba751075896471d14ffd50f4fde285af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5132784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bb4e1ecbe05a42b15e2f6bcc705de706124e85822c206467460c5adbb9122ca`

```dockerfile
```

-	Layers:
	-	`sha256:4c8d95caaa91e39296745f35e42f5fbf3b010d9ff90366e92ec383b1802ec655`  
		Last Modified: Fri, 08 May 2026 00:08:19 GMT  
		Size: 5.1 MB (5116794 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51637f14ff9eb616386fd12984ef305c13d13af40442dd8837d4860fd21f5a17`  
		Last Modified: Fri, 08 May 2026 00:08:19 GMT  
		Size: 16.0 KB (15990 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.4.1618-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:e7d7b11eadf6cad2688c85cb87d79c351105b844ad63cc6cd868f182e6d08633
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.5 MB (242533965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f2a429d9da22da9789d84efc5f319ed0b21a59beb0b5908b360a38e9a175a90`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1776729600'
# Fri, 08 May 2026 00:08:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 00:08:49 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 00:08:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 00:08:49 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 00:08:50 GMT
WORKDIR /tmp
# Fri, 08 May 2026 00:09:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 00:09:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 00:09:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 00:09:46 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 00:09:46 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:46ac7a0b9811e518f6b5a0d52940c913a1a560a8f78b82267804914e50244d2d`  
		Last Modified: Wed, 22 Apr 2026 00:16:03 GMT  
		Size: 28.1 MB (28116114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08898fba122ae67c0d338c8080fce95b2b114aa9fb84f7b9a4983f1fc75577f2`  
		Last Modified: Fri, 08 May 2026 00:09:25 GMT  
		Size: 144.7 MB (144724304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3455a864f16c9081f19c6372967a8892da2a1665b1f9d55d113a75e648a33db`  
		Last Modified: Fri, 08 May 2026 00:10:02 GMT  
		Size: 69.7 MB (69692507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8d7208796b032a3b473c0ac052bae2ab935b308e885f578e0c6b5cdc810e8c5`  
		Last Modified: Fri, 08 May 2026 00:10:00 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f673187fb2fea28e990abfb529cab7313a8130455f0035ca69fd8014ee37f04`  
		Last Modified: Fri, 08 May 2026 00:10:00 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1618-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:230fa169770581d6d368ec928090815d283efec64eeb4c54b11886afec6538fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5138663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27e72892ee492186857cb9603c38f858813f0d6c7abaf0a1fa978b0d804d4767`

```dockerfile
```

-	Layers:
	-	`sha256:12dd85f640dc94b0b59b6b705221a238bea542bb7a06c8d0f6f1d76e49058045`  
		Last Modified: Fri, 08 May 2026 00:10:00 GMT  
		Size: 5.1 MB (5122555 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:034e84c3eafda5cc7c0c8db70de0c69a453108665dfb2f9d225f3bc7ec87dd4c`  
		Last Modified: Fri, 08 May 2026 00:10:00 GMT  
		Size: 16.1 KB (16108 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.4.1618-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:d0b30308f77e7e24c8cd250221d25b9343e61f76ffd560f9f37c98ff07a71fec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.4 MB (253375791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7922f39d4c4b465d7890c74a6ea9ace92f08ea5a2591feea07504d9f00bdc8eb`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1776729600'
# Fri, 08 May 2026 00:43:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 00:43:06 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 00:43:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 00:43:06 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 00:43:06 GMT
WORKDIR /tmp
# Fri, 08 May 2026 00:50:04 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 00:50:04 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 00:50:10 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 00:50:10 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 00:50:10 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0bcb46f6315f7a2c8ddde875fca21de96c94e451046e6692f77a99aca489f3be`  
		Last Modified: Wed, 22 Apr 2026 00:15:02 GMT  
		Size: 32.1 MB (32078402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f1a630844f3ca330b4aeb3cf62ea83634554dfbe591d28cdf3d1bbe7c2c4aa2`  
		Last Modified: Fri, 08 May 2026 00:44:30 GMT  
		Size: 145.8 MB (145766245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1208c9a33910515c7ebe8a2ad6cc8daae6e8c1574a71a1e6235f89fca144d332`  
		Last Modified: Fri, 08 May 2026 00:50:48 GMT  
		Size: 75.5 MB (75530103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73020f5101389f1caacceb3a963e852f22a8db6995c58ab933df3aa9e0b5ca1f`  
		Last Modified: Fri, 08 May 2026 00:50:46 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:849cb1872f7a7b6040e25b46cafa38b3836f868c0bd8fe727e87e93b4a6b9bdc`  
		Last Modified: Fri, 08 May 2026 00:50:46 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1618-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:dd87fc22a464a9ac4899a97c8762ffaebda33294004e2890e23c1f0c3f4a54c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5137989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9673d2624fcd955d2b429eab0dfed47b87d1cc47bbc5b8d8fdbd68aa32f15caf`

```dockerfile
```

-	Layers:
	-	`sha256:915c60a12200cd3a1312cebd162bcbe69247eb3c60ec7d1130a70f55feb9f0f4`  
		Last Modified: Fri, 08 May 2026 00:50:46 GMT  
		Size: 5.1 MB (5121952 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe17a0e189cf4d67daa0acb8dfb290358ef6dd7391a22d0dbc29c7e1955858ea`  
		Last Modified: Fri, 08 May 2026 00:50:45 GMT  
		Size: 16.0 KB (16037 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.4.1618-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:910709dbfc5541e223d99fdba21f18c650c82e35902e56d0eed5bc08cea6806b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.3 MB (231315987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88f3b390de8034629b5bace2fed0355d837a285c03ed2215ad314eab727e49b8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1776729600'
# Fri, 08 May 2026 00:29:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 00:29:56 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 00:29:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 00:29:56 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 00:29:56 GMT
WORKDIR /tmp
# Fri, 08 May 2026 00:30:10 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 00:30:10 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 00:30:10 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 00:30:10 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 00:30:10 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:e579a0e0e7bfecd47e7766cad04eb36ba4b3ee329c3806a48d41d336705a1ca6`  
		Last Modified: Wed, 22 Apr 2026 00:15:36 GMT  
		Size: 26.9 MB (26891563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e2c106850671f417d6a753eb50a7f3a8baf38e8d040678d80497a6061af8bea`  
		Last Modified: Fri, 08 May 2026 00:30:40 GMT  
		Size: 135.9 MB (135910436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:730d4bb72bd360152516c27ab80aa6af7bcd63794ccde3deff9bcf965a2f8157`  
		Last Modified: Fri, 08 May 2026 00:30:38 GMT  
		Size: 68.5 MB (68512949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72ab120872204a26edd167dca0583181238cccd26f56a685467a26d001fa3aaa`  
		Last Modified: Fri, 08 May 2026 00:30:36 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7045730f3ad90a1b299d1e5e46829cc4290eedc9875cfe01b39a7cb62a81d4a0`  
		Last Modified: Fri, 08 May 2026 00:30:35 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1618-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:0fa5b15b3c4c0950ec064f5e4af116cb78deee7c152c998f17d5ebee8f02013a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5124105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e43395442f7186f8b5d352ae98ea74fcc8103105f1e5e7d6ff0d3164f102070d`

```dockerfile
```

-	Layers:
	-	`sha256:0686e875588d8a94a7a605391a940f5ec202c18690e071e3f4d49fcf4bf41087`  
		Last Modified: Fri, 08 May 2026 00:30:36 GMT  
		Size: 5.1 MB (5108115 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:712cb1c6a5dabb03af08e39b6eb4849b4f59000689d338a75c22c35fc7c63482`  
		Last Modified: Fri, 08 May 2026 00:30:35 GMT  
		Size: 16.0 KB (15990 bytes)  
		MIME: application/vnd.in-toto+json

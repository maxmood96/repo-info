## `clojure:temurin-25-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:23939a83471bf0a74c8d3a325ef118647e3a7ef7d1b9e0c33ddd66f45bd65193
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

### `clojure:temurin-25-tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:9f942ab26eeccd49c01d352ec652d27393f4066e7d7a7ae0cb17533571a25d4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.9 MB (189945214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d537e72f821c665848259aa68dff1a73d0c502011c8e87fa331417d70334d882`
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
	-	`sha256:5c32499ab806884c5725c705c2bf528662d034ed99de13d3205309e0d9ef0375`  
		Last Modified: Mon, 29 Sep 2025 23:34:35 GMT  
		Size: 28.2 MB (28228336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afefa26a7df6674ea9398356e2f35ef6f86527db1a008680c9dd0253b4f307ec`  
		Last Modified: Thu, 02 Oct 2025 09:54:13 GMT  
		Size: 92.0 MB (92036049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d6d0ffd9bb26ba4fd1469057b78011ac2e6b9147d919ecf48f1d7e875578d83`  
		Last Modified: Thu, 02 Oct 2025 09:54:11 GMT  
		Size: 69.7 MB (69679787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5f74b5e47307958b16eb5d052eaab6073de2c9882a07960beb829037100e1ce`  
		Last Modified: Thu, 02 Oct 2025 09:51:49 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cccede67f99ab96f1649f90c6cca4153c1274af8aeda3916f875e8e6a3c937b2`  
		Last Modified: Thu, 02 Oct 2025 09:51:48 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:616065ffc7fce14a10dbd37e8a8accbfe26673beb131a621c4486b2808142826
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5081301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8ca742932820dd1981c932416185afec47c96ed818931c0e224ec8df478b3cd`

```dockerfile
```

-	Layers:
	-	`sha256:39edb142e3ab1927a359ca5729e71986cafe506c6dea75b49b04018a3c4f4793`  
		Last Modified: Thu, 02 Oct 2025 12:44:04 GMT  
		Size: 5.1 MB (5064734 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df49172d2769ad3633bde7b3b5aa4c255086d4ada836c503f31157f24a50a743`  
		Last Modified: Thu, 02 Oct 2025 12:44:05 GMT  
		Size: 16.6 KB (16567 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:9cb8a3503038aba14ba29f4233522207833b89a27390613ade03f818ce49eaf5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.7 MB (188708704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0b8351f391895a278144449f3f9e904273572a94133a97f1a0d0423c0bea57f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1759104000'
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
	-	`sha256:f4e51325a7cb57cd9ae67bd9540483838b96bf7c9b0bf18205d9d30819e9ca38`  
		Last Modified: Mon, 29 Sep 2025 23:34:17 GMT  
		Size: 28.1 MB (28102145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:508113a26d3600e6b2b4524ae279079835d772ac78ebb985067513aba42edfb5`  
		Last Modified: Thu, 02 Oct 2025 02:47:20 GMT  
		Size: 91.0 MB (91045274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:687cd4fc91eea2eb52b668634b1672b629a5ec4867161da51382fbf5d9f0fb6b`  
		Last Modified: Thu, 02 Oct 2025 02:47:19 GMT  
		Size: 69.6 MB (69560245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56161aa178eebca8c4d64f3f2a17ea002b35485d64278d066a25e92cf6a9c01d`  
		Last Modified: Thu, 02 Oct 2025 02:47:12 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88f1df08665af22006646c9601f218b3262d8c059e2580a522162f7cc157df95`  
		Last Modified: Thu, 02 Oct 2025 02:47:11 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:fe281b840f6481178ebd7485ea3174ea42217c789ad32627b6802a2bd7512486
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5087226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61491320753033a39f09e98e3134e698fa5023e810442e4a9405fac0fc616d8a`

```dockerfile
```

-	Layers:
	-	`sha256:363bac26a8d7dc2aa968d0980604be99e495ba244d7ff1f46b2144814b916e5a`  
		Last Modified: Thu, 02 Oct 2025 06:46:03 GMT  
		Size: 5.1 MB (5070516 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:463f82ab6575ab097dd484494eb1602cb916dade3523f83f5a1a83203bb1c9a4`  
		Last Modified: Thu, 02 Oct 2025 06:46:04 GMT  
		Size: 16.7 KB (16710 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:38f211a759f1a756ba20e5b7bc636112706f26fd9355314952b7fb601db597de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.2 MB (199184321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:896708474dc709684caaca964b42a5fb28e9ee2e56e43dc80c4324c655cc5799`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1759104000'
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
	-	`sha256:2dae4fd387571f8090d4bc2fed08c7939fa2ac7aed0e2814aea4306333899e47`  
		Last Modified: Mon, 29 Sep 2025 23:34:09 GMT  
		Size: 32.1 MB (32068697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e858a4ba422d36407ccc76fd971eecfed15cbafb11a7b98b87ff00cd6065ba0`  
		Last Modified: Thu, 02 Oct 2025 09:32:28 GMT  
		Size: 91.6 MB (91601755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4db55f206707e2051faf66c539017b917051a913d1556f0439220e77294522bb`  
		Last Modified: Thu, 02 Oct 2025 09:41:06 GMT  
		Size: 75.5 MB (75512827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84988d78288eb815823f4798c215e1a3dc4ea55e495b58f18cf626862b3ab30c`  
		Last Modified: Thu, 02 Oct 2025 09:40:58 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0e02a71058132541eff3cd91d5376320a5062121bd9f340d4d83c0eb15cb70f`  
		Last Modified: Thu, 02 Oct 2025 09:40:58 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ca667995a80412912f12c3262a78e6a51d20f00e0df00055029c7dc03fc0de0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5087829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edb7d51793a1fcc4ced6606bed0170cd09c6969e48c156af8ec3d909901344bd`

```dockerfile
```

-	Layers:
	-	`sha256:bdf156103a96fb2bbe08d0c3fa831810ad4db132d02db9e7150cf278410c8783`  
		Last Modified: Thu, 02 Oct 2025 12:44:12 GMT  
		Size: 5.1 MB (5071202 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:888398c2f34466f48e4bffe55633d25fd19c5122f16ac3205794d739e93cb390`  
		Last Modified: Thu, 02 Oct 2025 12:44:13 GMT  
		Size: 16.6 KB (16627 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:2b84fb41d634eb6d206e179c74bc4b603a7b4041a2d80ac2a036d761dcc11394
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.6 MB (183582301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcd34fa0dbf773e5cc1754d72c6d74700d7fcaa752e06c09de60f0797c0274b2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1759104000'
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
	-	`sha256:ee23af7e2c95e7ad71a0f6edf7e138d45ffffb442811e2b9572806a68ee1338e`  
		Last Modified: Mon, 29 Sep 2025 23:34:05 GMT  
		Size: 26.9 MB (26884320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0da2f46b51187332c06e43a994b1544843b5a6c2414d403b93d8725d21e5f7c7`  
		Last Modified: Sun, 05 Oct 2025 05:39:48 GMT  
		Size: 88.2 MB (88206443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c13bd982c44325eeccab043e2692523078cd2a5298d197d1dcc0bbb9cf331312`  
		Last Modified: Thu, 02 Oct 2025 04:59:38 GMT  
		Size: 68.5 MB (68490496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da0ad52c902f022754ead42e5c9a589d75122ff6cb22a6e629f57c3f00d0b7f2`  
		Last Modified: Thu, 02 Oct 2025 04:59:23 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06b95a36e05680dcb681944d768fc2f0a2dee3e948ba43e258324caf7237ee67`  
		Last Modified: Thu, 02 Oct 2025 04:59:23 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a09e2eba8245f28017ea38916f7f7d8c825fe1ce7f7219112a7c9845ff0fdf66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5075171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2cdd47d175a3384bac7188f5ebac62d0e1dcdbd8bd9132d13b18006e0da3275`

```dockerfile
```

-	Layers:
	-	`sha256:53f9f50a8b5ca7acb3d6df34b126d700d0b146bb763d1d8fdfdbf4e1ba65ae7f`  
		Last Modified: Thu, 02 Oct 2025 06:46:11 GMT  
		Size: 5.1 MB (5058603 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f19620297e5a23abedcd6ff46437faaf925527358e7095c4d5099e85f8e8c20`  
		Last Modified: Thu, 02 Oct 2025 06:46:12 GMT  
		Size: 16.6 KB (16568 bytes)  
		MIME: application/vnd.in-toto+json

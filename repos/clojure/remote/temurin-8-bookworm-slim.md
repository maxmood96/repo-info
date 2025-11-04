## `clojure:temurin-8-bookworm-slim`

```console
$ docker pull clojure@sha256:4e2e21f471297aefbe3a472173f6fe2cbfdb1045a3a6e0d37acd74ff2a6d3a26
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:7b169ec90babbe1e85b404a3eb441d1dd2298f7fc017d79ff82f6c2b863f9aa8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.6 MB (152639855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fcadd5fb39779bff4f270dbdbd4ccc0f52ad2a397aa533a40bc059cd35e8dee`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:53:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Nov 2025 00:53:43 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 04 Nov 2025 00:53:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 00:53:43 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 04 Nov 2025 00:53:43 GMT
WORKDIR /tmp
# Tue, 04 Nov 2025 00:53:58 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 04 Nov 2025 00:53:58 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 04 Nov 2025 00:53:58 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:1adabd6b0d6b8acfa4ad149a984df0977135a7babf423538c7284a02744a4ee8`  
		Last Modified: Tue, 04 Nov 2025 00:12:15 GMT  
		Size: 28.2 MB (28228567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80b83644c3a315653dc4599f38f7fb025f404364a5c6c9634e3355dc600f27b0`  
		Last Modified: Tue, 04 Nov 2025 00:54:36 GMT  
		Size: 54.7 MB (54731291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f29bb31c54361e23982b667444e8461c032cdda201eaf09a71af403a528bb55`  
		Last Modified: Tue, 04 Nov 2025 00:54:38 GMT  
		Size: 69.7 MB (69679355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfdf01fdad54f054d4ed7c074f6029aa150e41482582ff80610dbbdfa2ce17df`  
		Last Modified: Tue, 04 Nov 2025 00:54:28 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:0d8994e745173d1559e91e595ede8cc49f8549a5ec2d9d063398464a4005a495
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5249246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5960fd93fe8ca95182ba3e5157933b3781ecd3e06f521118c4e03b0195b95e87`

```dockerfile
```

-	Layers:
	-	`sha256:185900f2bb7d1921aed787a936e400094eb7af016c048d60902d0570470d979e`  
		Last Modified: Tue, 04 Nov 2025 10:47:42 GMT  
		Size: 5.2 MB (5234998 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f2570a84c1d9819dde3ce5531861bee58ed456d65d6965de377ddf746db9a39`  
		Last Modified: Tue, 04 Nov 2025 10:47:43 GMT  
		Size: 14.2 KB (14248 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c24757afd157b370bffe6dd10ec6a087993b18a10e8eea43822cfeacbc30eee0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.5 MB (151498902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92593b382ef88203630f8023bc7bf68f719c6c25f432d7bdc0923efd63373f30`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:54:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Nov 2025 00:54:03 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 04 Nov 2025 00:54:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 00:54:03 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 04 Nov 2025 00:54:04 GMT
WORKDIR /tmp
# Tue, 04 Nov 2025 00:54:18 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 04 Nov 2025 00:54:18 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 04 Nov 2025 00:54:18 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:162e72af9357868b8f7f48fbf3ea23ddd179a309a9f28f2802a2e785239ec09d`  
		Last Modified: Tue, 04 Nov 2025 00:13:06 GMT  
		Size: 28.1 MB (28102376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8305024387475e0a878f887025d6d7dde5cf07862bade7b138366af80f0d6c41`  
		Last Modified: Tue, 04 Nov 2025 00:54:45 GMT  
		Size: 53.8 MB (53835605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa04c6b2bf0c0594296107b359009868131fcaac5f4300095b0ac17aff172160`  
		Last Modified: Tue, 04 Nov 2025 00:54:48 GMT  
		Size: 69.6 MB (69560277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf5be7035f8a58cebde07c9ed6c49ba534ed016495fcad46054341f9a71bfd25`  
		Last Modified: Tue, 04 Nov 2025 00:54:40 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:dc00c7e766cce2dff8e1be1afe384c072ff1d2e5a71661bb724666400d27431a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5255822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b148f86a1a8ed0a5683b5cb63491410c7a11622c20d88713d01b9bee63e65a42`

```dockerfile
```

-	Layers:
	-	`sha256:34bff5743006c2fbd3112016bb81480dcf266573b368a9eb9f2298170d5e77c6`  
		Last Modified: Tue, 04 Nov 2025 10:47:49 GMT  
		Size: 5.2 MB (5241457 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d108acd415551bb961ea7aea1ba228c722028f9392aa4e624a54334010321a75`  
		Last Modified: Tue, 04 Nov 2025 10:47:50 GMT  
		Size: 14.4 KB (14365 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:c01e59615a8917cf09c89b1b5c1edd24f9cd534a7d8d98e132312766d62a5d80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.7 MB (159747997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:299b602af8e500d4c42d47d0be40f74dce4e385c888f408870dd271378087f2a`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 13:00:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Nov 2025 13:00:28 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 04 Nov 2025 13:00:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 13:00:28 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 04 Nov 2025 13:00:29 GMT
WORKDIR /tmp
# Tue, 04 Nov 2025 13:06:05 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 04 Nov 2025 13:06:06 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 04 Nov 2025 13:06:06 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:2442ae4ed78d32124d4f8b92ec0b1caf0e12483bafbd1803659dc391d3600616`  
		Last Modified: Tue, 04 Nov 2025 00:13:59 GMT  
		Size: 32.1 MB (32068905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39313f2fa991c0ee72406327d7c1e060d584356d7b42935e8a92e8e96b03d37f`  
		Last Modified: Tue, 04 Nov 2025 13:01:49 GMT  
		Size: 52.2 MB (52165369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a31f595f9dd37610ca26a25934f30ee50f32fbcb2c5ac3f70dddd40bd887b96`  
		Last Modified: Tue, 04 Nov 2025 13:07:02 GMT  
		Size: 75.5 MB (75513080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18d7ef52a36c7b11628c63dd0460c9cf116727c60848b89aa88f7d3483aa1b3a`  
		Last Modified: Tue, 04 Nov 2025 13:06:55 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ae29f27330db6dd18ca929d0cdcede2df96d2a3fe63ac754689997a7da11acb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5254244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d28fb733e550a33b80c36d6839eb43a3fb9571e1951e4494667e207add14e3ba`

```dockerfile
```

-	Layers:
	-	`sha256:391ee978c236fa1b2cca3ac9bb27480708ce58094d1d1d91e5bbb6efcf86af0f`  
		Last Modified: Tue, 04 Nov 2025 13:38:29 GMT  
		Size: 5.2 MB (5240749 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d845b633f483f6a7cb0120ae448ded102a95551ea9c91d048d6ab0ebc2686b58`  
		Last Modified: Tue, 04 Nov 2025 13:38:30 GMT  
		Size: 13.5 KB (13495 bytes)  
		MIME: application/vnd.in-toto+json

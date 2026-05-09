## `clojure:temurin-8-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:81895d996cef63b4a259b909d39f25f291381c61089d9fd36c2fbb6f5c61561a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:12e0a2251d43f5b02985f5f92820e62665163251cf0158c001b5470d957bab8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.1 MB (153106032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bd18c29878c9eac0ab8d12745811b4e7d29266837c8781093586cba06f9023e`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 20:14:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 20:14:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 20:14:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 20:14:36 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 20:14:36 GMT
WORKDIR /tmp
# Fri, 08 May 2026 20:14:51 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 20:14:51 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 20:14:51 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:9b02e9fcb40102eae20d9d1fc7594b44328f4a3eb9b8a3bdb7db283d10840a30`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 28.2 MB (28236282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9934f8b55f14c72b1b04b97731dcf70c14434fc71d7228540acab88cd552149b`  
		Last Modified: Fri, 08 May 2026 20:15:09 GMT  
		Size: 55.2 MB (55170061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f55b856bcff59ee4f0d8bed446461a067a153625903490b5c13ade7c0e2310b6`  
		Last Modified: Fri, 08 May 2026 20:15:09 GMT  
		Size: 69.7 MB (69699043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d993d52c851eaacfeaafea76a464661bee078da2bdce24d5183ddd054e73a337`  
		Last Modified: Fri, 08 May 2026 20:15:06 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:3389a9aa8a8af4422dde8d2e265a43e1c08c80f7825fa0940ae752e502b7d8c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5251402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ffdfcfa1497805a9c7f21d1e66a960043c65b8521901dd12b7cb360fd2a22bd`

```dockerfile
```

-	Layers:
	-	`sha256:0876733247b6fc738d99744e961198a5f50aacfd9b6a14f9e2a9ee12714216d6`  
		Last Modified: Fri, 08 May 2026 20:15:07 GMT  
		Size: 5.2 MB (5237154 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32e8cc8e37b3029d9ee84cf949e8495e83fcb8aa6015d5806b8e73da9ca80cfa`  
		Last Modified: Fri, 08 May 2026 20:15:07 GMT  
		Size: 14.2 KB (14248 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:7fd1be3a40afd8a0f89777e59a04dd89db75cbeba2b7e014dfea06c0a7dcc123
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.1 MB (152061004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5917c0238b45a96ff94acdb47421c372c237a10925f50a06c91f3761b35387c8`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 20:18:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 20:18:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 20:18:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 20:18:14 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 20:18:14 GMT
WORKDIR /tmp
# Fri, 08 May 2026 20:19:07 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 20:19:07 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 20:19:07 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:6a2d07df495cc055bce0251fe801ee08db90750f52e43a555be5dfd8f5023783`  
		Last Modified: Fri, 08 May 2026 18:24:52 GMT  
		Size: 28.1 MB (28116165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90d3fc2979e5e360a31f9c76b1ed6dc7fe19f9743a5e50f739a5848268e42445`  
		Last Modified: Fri, 08 May 2026 20:18:44 GMT  
		Size: 54.3 MB (54251615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e58b04b659ccc05131b38c29c86b62be2893d0cf448149c2bd56a8dc9bc39838`  
		Last Modified: Fri, 08 May 2026 20:19:24 GMT  
		Size: 69.7 MB (69692578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df1d8170408f115caf799c6fc9a4ff46d4bb6a0e2a5bd516785be086d0ea0dea`  
		Last Modified: Fri, 08 May 2026 20:19:22 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:6bc5aa0501dd9c31838d03668f6687cb60c0638ae95c03e4fe21d64e00221a23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5257181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c63e8fbc292a5cfd27e504a0ecad5f0ed8063ac2814bb7fba205fceceeb7c5b`

```dockerfile
```

-	Layers:
	-	`sha256:44fdd52e28367dcce3523302d2df07608b491a5a57130bc9762c19e4234affa4`  
		Last Modified: Fri, 08 May 2026 20:19:22 GMT  
		Size: 5.2 MB (5243615 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b0fdf0f41e313262879c08702ecbdac86608763009cd68bf601378287d4d051`  
		Last Modified: Fri, 08 May 2026 20:19:22 GMT  
		Size: 13.6 KB (13566 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:2bb43348ff3591fc34aac6844bf5ac9e8e97a2a53f861ac2877cbf8ca1c42901
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.3 MB (160259266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2069b6dcbed07e2175ce27a22f0c8abe75672fd9fd539cb0f1efc48cdb03c9b`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1777939200'
# Sat, 09 May 2026 02:20:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 09 May 2026 02:20:44 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 09 May 2026 02:20:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 09 May 2026 02:20:44 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Sat, 09 May 2026 02:20:44 GMT
WORKDIR /tmp
# Sat, 09 May 2026 02:23:31 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 09 May 2026 02:23:32 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 09 May 2026 02:23:32 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:0e29ea7436ed4beb1c38bcfee44589407e49fc690669b42b35db33a9588e820a`  
		Last Modified: Fri, 08 May 2026 19:44:06 GMT  
		Size: 32.1 MB (32078453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0646e96975a751e4abef1f39bda50e33740041680512c6868770fa73e204ade0`  
		Last Modified: Sat, 09 May 2026 02:21:39 GMT  
		Size: 52.7 MB (52650396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f1b1842417c5c974adf8892145eb621e4fdeb7f0c8aa216171c60696447801f`  
		Last Modified: Sat, 09 May 2026 02:24:01 GMT  
		Size: 75.5 MB (75529770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5f54a0eb4e590a8f2ff88a1ff9657f1ce2d60c8b8af7608e0a54f75c288363e`  
		Last Modified: Sat, 09 May 2026 02:23:59 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:875554825fbcf08b24bbf33df601c08972e8117d09314056ff21c0beb8080619
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5257203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a6aef0ee590f6b81f2b1f4cb2f11ddeed81e9de70292717183619b32bdd2052`

```dockerfile
```

-	Layers:
	-	`sha256:c5a71bb941e1295180af3e6a079975ffa2361fe01ba0cc9023921df9fab79525`  
		Last Modified: Sat, 09 May 2026 02:23:59 GMT  
		Size: 5.2 MB (5242907 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9df22fcb0ee2d22eae08708c9387f661c96e34941c7deee5bcb7bb6fc80a3d4b`  
		Last Modified: Sat, 09 May 2026 02:23:59 GMT  
		Size: 14.3 KB (14296 bytes)  
		MIME: application/vnd.in-toto+json

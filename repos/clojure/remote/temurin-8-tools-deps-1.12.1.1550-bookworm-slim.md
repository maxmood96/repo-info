## `clojure:temurin-8-tools-deps-1.12.1.1550-bookworm-slim`

```console
$ docker pull clojure@sha256:0cbed2fcf6826e02c403449a00fe4b8f41af915b466285b753ca2808b17010c3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-1.12.1.1550-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:9ff0b1db95c8b727d30ebef22a77ae89058a4f06701954e5a9da8e67e5768f1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.5 MB (152480122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07185b6745e1d4450b50debb726592f08dbd03eb3a4b244e55cf00b36fe1adbf`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
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
CMD ["clj"]
```

-	Layers:
	-	`sha256:3da95a905ed546f99c4564407923a681757d89651a388ec3f1f5e9bf5ed0b39d`  
		Last Modified: Tue, 01 Jul 2025 01:14:43 GMT  
		Size: 28.2 MB (28230143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee67e87bc34a283d13189c69f6915f6d99b1b6d195c83b2a572dd211d08593a8`  
		Last Modified: Wed, 02 Jul 2025 04:15:50 GMT  
		Size: 54.7 MB (54716197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9feb87dc4ca32c04c9a2c4a540843099939e595e18e5f550df3956dd0118db02`  
		Last Modified: Wed, 02 Jul 2025 04:15:50 GMT  
		Size: 69.5 MB (69533139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f3e61995e1e1b16eb5a32727afd515a4cc804e5bd96dee7e486d9aef774eecb`  
		Last Modified: Wed, 02 Jul 2025 05:44:09 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.1.1550-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c7077ee3b24bf82f43b8cfccee6b348f58202f805620192a92919e18ebca3080
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5247145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8090bb4a58b06d4609e4671dcc9b9bfbf62258bcfa44b4f5586031c1696f188`

```dockerfile
```

-	Layers:
	-	`sha256:c3caa5090e08754bf7d3dd65ec902c7ad642e9b91b0de6689ba1001af6cf0934`  
		Last Modified: Wed, 02 Jul 2025 06:42:56 GMT  
		Size: 5.2 MB (5232854 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55bb3806842bad35d075b537000b392dd0af1a3e362b5d3cca153fdd60a356db`  
		Last Modified: Wed, 02 Jul 2025 06:42:57 GMT  
		Size: 14.3 KB (14291 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.1.1550-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:f029d4bdab68c54eb969bbe6a7e0aa9f65387d524387227ea97dff03ec409640
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.3 MB (151297441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4fe9c1b587188d5eecf4d6a9ff050573864f7b5470eface4e23a8af19d63b5c`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1751241600'
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
CMD ["clj"]
```

-	Layers:
	-	`sha256:37259e7330667afd74c3386d3ed869f06bd9b7714370c78e3065f4e28607cc02`  
		Last Modified: Tue, 01 Jul 2025 01:15:09 GMT  
		Size: 28.1 MB (28077678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44c679baa0c56e50c43f0884e8844d0fbb7c9898866aa0b1eddbc7c174c0a53b`  
		Last Modified: Tue, 01 Jul 2025 13:20:49 GMT  
		Size: 53.8 MB (53830509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed5bbf3e84c56b067405ee1153cb319c6bda7cb8707c4e64bbc0959e6dcc7697`  
		Last Modified: Tue, 01 Jul 2025 12:01:57 GMT  
		Size: 69.4 MB (69388609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f3984be063b2c20c6e5d5d94aadb8d51adc643b0bee7d57b6328bec81865bb8`  
		Last Modified: Tue, 01 Jul 2025 12:01:54 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.1.1550-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b9cb78650cfac728c0f44fe69c1223b469e8c85ea441305b57ac7a9d4d331c37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5253722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ca52cacc0ddc58b084286620abd5a3d609fb902c1a10e2c4a46db79025e34c0`

```dockerfile
```

-	Layers:
	-	`sha256:9643062f870d88264ad77d8b855e6917d3ddb56cc33180b0ef4ccc4e9aa48231`  
		Last Modified: Tue, 01 Jul 2025 12:38:44 GMT  
		Size: 5.2 MB (5239313 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e9ba82e8da46d99ff5dd95b4ebe6b79aefd657a2ff3103f5dbf191a4f6d24a2`  
		Last Modified: Tue, 01 Jul 2025 12:38:44 GMT  
		Size: 14.4 KB (14409 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.1.1550-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:285e51cbe07deafde08e59a9a21e57c1d9cbc939d366a6418558a4a183b4feb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.6 MB (159599971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ff9ac4064ab5b40d67f112c5799c110fdda6e3712e44cd8f655451e7ebdb1b9`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1751241600'
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
CMD ["clj"]
```

-	Layers:
	-	`sha256:c5884d20b08634214a92bd5de559876bf30e6c5453807c3014f5480eeba20662`  
		Last Modified: Tue, 01 Jul 2025 01:15:20 GMT  
		Size: 32.1 MB (32072820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0942298fc2abdf69cf3e6a970afc1659ec0c0948df86dc3a34aacc3e87a41dca`  
		Last Modified: Tue, 01 Jul 2025 08:16:09 GMT  
		Size: 52.2 MB (52167961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:688306c19214c9f446d35e2e3713caaf3997eb659fc03c85b865fa5052a7c37b`  
		Last Modified: Tue, 01 Jul 2025 13:20:56 GMT  
		Size: 75.4 MB (75358545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59b2dbb8ef4334ee0523f4fed8493942756aec3b6b4b056328a69048ac712aa5`  
		Last Modified: Tue, 01 Jul 2025 08:23:54 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.1.1550-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:359bf5b4ee8e679f2603811269de94c83227968ab81cd882ab604c8b1f7562aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5252944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67da6a052a6f0f58d2ae782afd593ffabb1f324448d6241ff9d48349eb551cd6`

```dockerfile
```

-	Layers:
	-	`sha256:033856111456f8cf09922b6514f525f2a4d957f4d8719ad24858c22cc845e9d5`  
		Last Modified: Tue, 01 Jul 2025 09:42:03 GMT  
		Size: 5.2 MB (5238605 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:856c6a81f7a53b3bf75dcbe7d5fc966d413623f8b645a31a93410ea6ad68f36e`  
		Last Modified: Tue, 01 Jul 2025 09:42:03 GMT  
		Size: 14.3 KB (14339 bytes)  
		MIME: application/vnd.in-toto+json

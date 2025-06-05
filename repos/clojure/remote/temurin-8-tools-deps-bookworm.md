## `clojure:temurin-8-tools-deps-bookworm`

```console
$ docker pull clojure@sha256:c5af24ecc66059ca601858fb8e315b14ab320bf102c8b7c2ba974a65f314ef29
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:712f7e4c47200b55531b5c8fa3803fb6b9b9cfdabfb5454d200dfec0935f13be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.2 MB (184199133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd10ccc82d14e8bc7364c969abd008d92a7327bdb72b4359db72777f9721503f`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
# Tue, 03 Jun 2025 15:45:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Jun 2025 15:45:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Jun 2025 15:45:26 GMT
ENV CLOJURE_VERSION=1.12.1.1543
# Tue, 03 Jun 2025 15:45:26 GMT
WORKDIR /tmp
# Tue, 03 Jun 2025 15:45:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "09b7b8185b8a35b1ddcc9c2a5155d094fe1237805c24489312f3e324a83b0d4c *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:3e6b9d1a95114e19f12262a4e8a59ad1d1a10ca7b82108adcf0605a200294964`  
		Last Modified: Tue, 03 Jun 2025 13:30:19 GMT  
		Size: 48.5 MB (48488245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bae221cd6eaafce56d944befe65002cbf3f76f3499f3e07ef01191d1b325586`  
		Last Modified: Tue, 03 Jun 2025 18:24:18 GMT  
		Size: 54.7 MB (54716181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:902e2f77a0f0e75ca6e841363f9b59516ab9b15fbcddc851cb5536af7f42072a`  
		Last Modified: Thu, 05 Jun 2025 01:41:40 GMT  
		Size: 81.0 MB (80994063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ce8af1c2264e463e05c912a48366badc12c3ff5aa31ab0bb08d3069505c5ce1`  
		Last Modified: Thu, 05 Jun 2025 01:41:35 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:3982e69c3bdabadecba89d82b6a3bacae84edb41a77dff6713540f0b52c28d54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7354369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49bf386f7ea0afb0c9984f42856b6fc10d58cf35fcc6eec87017890df46a7316`

```dockerfile
```

-	Layers:
	-	`sha256:cef2ae1b08d48a0bc71985353dcc4a82bfcbb13f6953adb3c1498a36eb0d1ead`  
		Last Modified: Tue, 03 Jun 2025 21:44:14 GMT  
		Size: 7.3 MB (7340132 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0495f2df71ea155f00d0dad4e3aa0f2890806fc7ae13bda09b3fe3c30ba10f97`  
		Last Modified: Tue, 03 Jun 2025 21:44:15 GMT  
		Size: 14.2 KB (14237 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:291b52d6ab6bd4a1f492788d4285109023b016818ac4c8c37565f7940c70376d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.0 MB (183007620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4030dc9914a9ed2e54583e55246dc373e9471efaf2929c16cf24c10ae15ac35f`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
# Tue, 03 Jun 2025 15:45:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Jun 2025 15:45:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Jun 2025 15:45:26 GMT
ENV CLOJURE_VERSION=1.12.1.1543
# Tue, 03 Jun 2025 15:45:26 GMT
WORKDIR /tmp
# Tue, 03 Jun 2025 15:45:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "09b7b8185b8a35b1ddcc9c2a5155d094fe1237805c24489312f3e324a83b0d4c *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:1a12b4ea7c0ce04aa0e98be0a8c9942162bac71426f734fe6d3bf988bc9e2627`  
		Last Modified: Tue, 03 Jun 2025 13:30:16 GMT  
		Size: 48.3 MB (48327181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cd4992357ba318e5480f8b56ec256a277c565a89898891e78871d47ce9c0350`  
		Last Modified: Tue, 03 Jun 2025 19:25:26 GMT  
		Size: 53.8 MB (53830497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74af05c2e16bed95729e4691d49a37f4f67f7619550c94a1e83122127fad8976`  
		Last Modified: Tue, 03 Jun 2025 19:25:34 GMT  
		Size: 80.8 MB (80849296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d0b416564c1d25bf95c5eaced13607dfa719e9ef4dd6904516af281120e0981`  
		Last Modified: Tue, 03 Jun 2025 18:29:35 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:0b8f3c1c834ba57e7ecbeed28322ba875259843f636209f88743521101f6d0eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7360948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13c3b0ae520c860d4f5ad53798e0ffbed4fd7816b8a9070f497750e31fcc1073`

```dockerfile
```

-	Layers:
	-	`sha256:053e97084cf5c6b47e61360cdb4e32f9a9860572d181904483f3b544db8509e4`  
		Last Modified: Tue, 03 Jun 2025 18:37:07 GMT  
		Size: 7.3 MB (7346593 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27904c1142cef69440498166aeb0a8c09d6344a54af8cfb44b42b5346f717722`  
		Last Modified: Tue, 03 Jun 2025 18:37:08 GMT  
		Size: 14.4 KB (14355 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:e7ef13bd7d59c2ffb717ee4c3503fce86635fcb5ea9c5dd059e05e1f37ffecae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.3 MB (191313354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c16a994896ceed0d14b8e15de4b592e0342d76874bb9c36ad1e9e353a392dea`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1747699200'
# Tue, 03 Jun 2025 15:45:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Jun 2025 15:45:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Jun 2025 15:45:26 GMT
ENV CLOJURE_VERSION=1.12.1.1543
# Tue, 03 Jun 2025 15:45:26 GMT
WORKDIR /tmp
# Tue, 03 Jun 2025 15:45:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "09b7b8185b8a35b1ddcc9c2a5155d094fe1237805c24489312f3e324a83b0d4c *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:996840ee350796081b3c80118ca1a58ce8212c6fdf88c454706a16457903a0c9`  
		Last Modified: Tue, 03 Jun 2025 13:33:40 GMT  
		Size: 52.3 MB (52331619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e5db02309f6380af00f3a055d44f88afac6c886fbdca776378625bc23fbf4af`  
		Last Modified: Tue, 03 Jun 2025 20:16:40 GMT  
		Size: 52.2 MB (52167966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:284bbec8eaa03ee9d88f455951ae4b6105cf3c01f5a50888c9bdb95d5ea5bf76`  
		Last Modified: Tue, 03 Jun 2025 18:28:59 GMT  
		Size: 86.8 MB (86813126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9b1d6416bf34b3db9bee1923f9c60c047065581c6ce6f159e9aa15ab871e614`  
		Last Modified: Tue, 03 Jun 2025 18:28:44 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:71c599624cea3ada7050a893f7e51c09adf29dcf9d704120c27975e303927a93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7360213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e616022c6cf886e7e43c179f621021a05808bb9c159b259128714ca0c8dd12a`

```dockerfile
```

-	Layers:
	-	`sha256:301f518f1ebebb71866d184d79701578854e3f52509e6f94e9c0031225b2d433`  
		Last Modified: Tue, 03 Jun 2025 18:37:15 GMT  
		Size: 7.3 MB (7345929 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1d7e1475644f7038f88ffde9ed7e90866926ff3d656feb91290d35249932e56`  
		Last Modified: Tue, 03 Jun 2025 18:37:15 GMT  
		Size: 14.3 KB (14284 bytes)  
		MIME: application/vnd.in-toto+json

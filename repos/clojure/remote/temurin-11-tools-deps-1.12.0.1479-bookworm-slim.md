## `clojure:temurin-11-tools-deps-1.12.0.1479-bookworm-slim`

```console
$ docker pull clojure@sha256:b676602f16df0048b155f29acfae53a0c4e0fc1715a0c585d9354093682dcf73
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-1.12.0.1479-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:a498bfb78e2c727b04873087d07a43c4cc9df1effd7f750c0e0c0bc22daf730e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.2 MB (244217074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db34f630e43a71edaa8ea5b43f8289fe33ecef0c9e5ec99077de45945ed365b8`
-	Default Command: `["clj"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["bash"]
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:2d429b9e73a6cf90a5bb85105c8118b30a1b2deedeae3ea9587055ffcb80eb45`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 29.1 MB (29127995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16924935036548fa95a02683aa5d1add89142f550af9728b746c4590c02a3b11`  
		Last Modified: Tue, 12 Nov 2024 02:23:43 GMT  
		Size: 145.6 MB (145601329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d6d715b25524740f3f263d2cd12eb21e9052a2e71d8473cfbd29442a26abe16`  
		Last Modified: Tue, 12 Nov 2024 02:23:42 GMT  
		Size: 69.5 MB (69487107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f932dc65acad4e43ba9e8b67dd6f93713891b99c55d107f965afdb6e7880f9b`  
		Last Modified: Tue, 12 Nov 2024 02:23:41 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.0.1479-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:f791e11ab4e67a03f1d7f9e08fefe752242ae79a4a4677240858a91cf5a773d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4955109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c508220ca6ecb38b7bf84d6d3cee6f7e36174a0c6b8bb7d2ceb913c7e27b23e6`

```dockerfile
```

-	Layers:
	-	`sha256:13b40adddb809205d1a9719841334d24ae84df7d1991624ea4c03fcf5a95ed0a`  
		Last Modified: Tue, 12 Nov 2024 02:23:41 GMT  
		Size: 4.9 MB (4940799 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a446804ead9ebbb785b9446d7dd9b00cd1e4dfa4b21baacf8556fe844729959`  
		Last Modified: Tue, 12 Nov 2024 02:23:41 GMT  
		Size: 14.3 KB (14310 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.0.1479-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:e5c077f3cc72d59ca5166f29f5411c45f51c8c0bfc425b00cf4f7e0e05c3bb5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.9 MB (240891496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26d5aa3e982f979d88a41e5d9b35d93e61140613477508c92321364fccb141ab`
-	Default Command: `["clj"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD file:702193928cded0bcec5edbf4a5660961e7caef8c9d9cafea3337b7f6720c4464 in / 
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["bash"]
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:83d624c4be2db5b81ae220b6b10cbc9a559d5800fd32556f4020727098f71ed0`  
		Last Modified: Thu, 17 Oct 2024 01:14:39 GMT  
		Size: 29.2 MB (29156341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f9c9542bb5c24b01cc4444fc921ba60e64bde0acc844aa27de102d3306ab810`  
		Last Modified: Thu, 24 Oct 2024 09:04:12 GMT  
		Size: 142.4 MB (142389159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:994ae9f49fa9841ade8271e455e18d7ca999faa1d0806d5e4d7d320a06096e5f`  
		Last Modified: Thu, 24 Oct 2024 09:09:46 GMT  
		Size: 69.3 MB (69345350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcda3d8c86dedcb38ce900a99fb66e6511adca034d8f98bb1215d8724bd77dbb`  
		Last Modified: Thu, 24 Oct 2024 09:09:44 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.0.1479-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:95ef02538c69fb59eea9d43b4605f0f2154f9c3b61f00371502ad4f7f325b00c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4961402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2bbd7eeaf963cda30885faa12beb108b8e831f8cc4f8c0fd2347cce3f62bf31`

```dockerfile
```

-	Layers:
	-	`sha256:cb73bc7a894c98d2469bc4f7d625491888b5cb8721db099dec5d93da8ad5d5b1`  
		Last Modified: Thu, 24 Oct 2024 09:09:44 GMT  
		Size: 4.9 MB (4947148 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d6780393282137e0d6c50fa2e74dc74dbdbefe0786a78197093001012f9a035`  
		Last Modified: Thu, 24 Oct 2024 09:09:43 GMT  
		Size: 14.3 KB (14254 bytes)  
		MIME: application/vnd.in-toto+json

## `clojure:temurin-8-tools-deps-1.12.4.1602-bookworm-slim`

```console
$ docker pull clojure@sha256:fd6b440d1b78b7717f6e45c5e28ef687a90dcd4480ee52114efc19b1da4026ba
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-1.12.4.1602-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:df3e4dd75c9dd9bf70be838fe9574ffeebcf7ca9ab8e56b5b03c5aad709dde93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.1 MB (153076910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cc9fb951c35fa7d942afc44eaee63cf3fed27115a8cf9fa9952b5f7bfe14216`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 17 Feb 2026 21:40:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 21:40:03 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 21:40:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 21:40:03 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 17 Feb 2026 21:40:03 GMT
WORKDIR /tmp
# Tue, 17 Feb 2026 21:40:54 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Feb 2026 21:40:54 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Feb 2026 21:40:54 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:4831516dd0cb86845f5f902cb9b9d25b5c853152c337eb57e4737a9b7e2a2eb9`  
		Last Modified: Tue, 03 Feb 2026 01:13:33 GMT  
		Size: 28.2 MB (28228487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2127a5b0313b208164d6181d5cefdadd769f5110a05b1d4ab3b4976d8121becc`  
		Last Modified: Tue, 17 Feb 2026 21:40:32 GMT  
		Size: 55.2 MB (55170110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6960e09edf0cb1687e434af1cab446f016da9673a5deaecf1779a570bf6c6cdb`  
		Last Modified: Tue, 17 Feb 2026 21:41:09 GMT  
		Size: 69.7 MB (69677666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19a727e41dec666978c89b1c69db975e84c282cd957c16aa8490595d66cf1855`  
		Last Modified: Tue, 17 Feb 2026 21:41:07 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.4.1602-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d12a78658ea783beab5fb0b3721e3b3b19dd8d64c353d26c5d8c81b956db9824
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5249889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9e40d58e4e867d8ee70599b4db6bd7670ee6d1ae46b72e399e030f6b70947d4`

```dockerfile
```

-	Layers:
	-	`sha256:28e110cd82dbaa3cff0735673d6c9db8a6b2ea9fc04199697175b522b1bc0e37`  
		Last Modified: Tue, 17 Feb 2026 21:41:07 GMT  
		Size: 5.2 MB (5235641 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee42c54e9e9fe2b3bbb098a1468c0c1e13cfb1969c75939a02f6ef00bd82f2c5`  
		Last Modified: Tue, 17 Feb 2026 21:41:07 GMT  
		Size: 14.2 KB (14248 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.4.1602-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:39c9b33602899002632e9f7a9ebeeb998c41ccbe9f43a734ca14a9234441a268
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.0 MB (152032757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9723ce753242c444b1a61797c08b78372b61c1a5677863dab45aac2a105065f`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1769990400'
# Tue, 17 Feb 2026 21:40:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 21:40:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 21:40:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 21:40:33 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 17 Feb 2026 21:40:33 GMT
WORKDIR /tmp
# Tue, 17 Feb 2026 21:40:48 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Feb 2026 21:40:48 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Feb 2026 21:40:48 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:d3d5d8ab26d25b9040a3c2160d7ddfe3911ae81035d5b1b0904f3ebda32476b6`  
		Last Modified: Tue, 03 Feb 2026 01:13:36 GMT  
		Size: 28.1 MB (28107823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09727984b85efe00778435d1debfc0866726d5833ef72fb62b560690926084a8`  
		Last Modified: Tue, 17 Feb 2026 21:41:05 GMT  
		Size: 54.3 MB (54251610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66d41298ee479f55e42b9dfd1445ca32f761fd32a9ecbaacff4c5c4251818fa9`  
		Last Modified: Tue, 17 Feb 2026 21:41:05 GMT  
		Size: 69.7 MB (69672680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce3ce2e77d918f21d4ba06f6de4f980ad7e32c1e4395665487fa9231d14d8d91`  
		Last Modified: Tue, 17 Feb 2026 21:41:03 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.4.1602-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:91d54bcdf07105369386dd201919a5e604b93c8af290e92a4f3cee6d7f2b8460
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5256468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09b9e1a5c60e8f8e201e68e332d52dcadb44037e796fc3db307a4a0f738c1a2d`

```dockerfile
```

-	Layers:
	-	`sha256:2f51b36308fd2914370f1ed1b4d840cfcab51e79bcc849205dcb116ffb67058e`  
		Last Modified: Tue, 17 Feb 2026 21:41:03 GMT  
		Size: 5.2 MB (5242102 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f4fdaac6179ff46fd730c2a2c00954989134bdfc791575e7a7c31e73630d5a3`  
		Last Modified: Tue, 17 Feb 2026 21:41:03 GMT  
		Size: 14.4 KB (14366 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.4.1602-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:2a6289b2828a7520a9bf6c485235fb27562b2d3165449ef82a9371fe93630f10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.2 MB (160233858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:720f71bb14575c2b07a6f244cb34a91308fcd07c959ba918dcd240847b44a1b9`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1769990400'
# Thu, 05 Feb 2026 23:57:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 23:57:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 05 Feb 2026 23:57:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 23:57:25 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Thu, 05 Feb 2026 23:57:26 GMT
WORKDIR /tmp
# Fri, 06 Feb 2026 00:03:53 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 06 Feb 2026 00:03:55 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 06 Feb 2026 00:03:55 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:7910825c7ec7b68916beacd9af906d34dec10e730af19f67c87aa4e2ee440381`  
		Last Modified: Tue, 03 Feb 2026 01:12:56 GMT  
		Size: 32.1 MB (32068712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4fdf83ffd1238f33e1fa3f93bce20dfbfd9ae745a5f61042a0bc95827efbd6d`  
		Last Modified: Thu, 05 Feb 2026 23:59:00 GMT  
		Size: 52.7 MB (52650394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8a3dc37174143c3e49846ed024e124c88f9671c47fd5d699f75ca97b876fc4c`  
		Last Modified: Fri, 06 Feb 2026 00:04:36 GMT  
		Size: 75.5 MB (75514106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:373f1f68513648509379b8064b9669cd2c188bdfd8d4157a589dd8ba8ff5d800`  
		Last Modified: Fri, 06 Feb 2026 00:04:34 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.4.1602-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:72e9ff8d1390b22f029d2ce2de0cc272a103049cf9df383524f61db07fd8c6a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5255687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a23cb8417544cce2ea3b17592ab355cabe0ab5937e95f90e102ea51980ca0c52`

```dockerfile
```

-	Layers:
	-	`sha256:9adb58dd3edfa54976be8253c25b53230fdc6a9d9d10041c2782566e934f2e60`  
		Last Modified: Fri, 06 Feb 2026 00:04:34 GMT  
		Size: 5.2 MB (5241394 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0716f85215c2867097dd0185cdf3cd29b72cd0a66dacfd6293d6c55c978ce88a`  
		Last Modified: Fri, 06 Feb 2026 00:04:34 GMT  
		Size: 14.3 KB (14293 bytes)  
		MIME: application/vnd.in-toto+json

## `clojure:temurin-8-bookworm-slim`

```console
$ docker pull clojure@sha256:10a1595d105aa6fc4e04fc7452f8cae39830a5befff292a0c8cf8a77868ad2e2
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
$ docker pull clojure@sha256:b1e1b326c10340e3b84fbddac22bcb2d76e8cebb1fc16cd2c50979a20773e44a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.2 MB (153165494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3ead2cf80d6014572f03b7fa5f1d673d2e9ee16898fe4a228595e462ee618ca`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Fri, 15 May 2026 20:12:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 May 2026 20:12:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 15 May 2026 20:12:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 20:12:51 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Fri, 15 May 2026 20:12:51 GMT
WORKDIR /tmp
# Fri, 15 May 2026 20:13:06 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 15 May 2026 20:13:06 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 15 May 2026 20:13:06 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:9b02e9fcb40102eae20d9d1fc7594b44328f4a3eb9b8a3bdb7db283d10840a30`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 28.2 MB (28236282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7256dbf5d236827b689b54a74736d5f33f7574512859e268d673ce9f170e330`  
		Last Modified: Fri, 15 May 2026 20:13:24 GMT  
		Size: 55.2 MB (55198725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0901864efb74bdc2fff7a4d6368ba764290e982a14bfebac770eec9473871c0f`  
		Last Modified: Fri, 15 May 2026 20:13:25 GMT  
		Size: 69.7 MB (69729841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0128e5f1d91c51d153bd936940a6a33af3bc935936efdd1bf66c19f770d0561`  
		Last Modified: Fri, 15 May 2026 20:13:21 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:873e962a1d704661b6d172f2813669ff6172bd01cbefcfc8ac1036f4c7346ce2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5251554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68ab07d8d057d50ea46f8028415cc2fccccaf2cd1eff4e047f0c008d1c48cc80`

```dockerfile
```

-	Layers:
	-	`sha256:4dcb1bd79f6c6d6c808d856cae6ef72ff2a1fe5d5a16303fe52f220288a34ff6`  
		Last Modified: Fri, 15 May 2026 20:13:21 GMT  
		Size: 5.2 MB (5237152 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe7e39d6511156df3536a7b981a33183c5ea1f68b7b9826d579b1edc4f0c6eac`  
		Last Modified: Fri, 15 May 2026 20:13:21 GMT  
		Size: 14.4 KB (14402 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:668332daf426a847b6c533b9199e1c93bca60a159d76e31192f58b8073195c79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.1 MB (152112395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c93111c46b2dac78e8e20225254b8f125180e46ba95579fc99f16df74a167bee`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1777939200'
# Fri, 15 May 2026 20:12:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 May 2026 20:12:53 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 15 May 2026 20:12:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 20:12:53 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Fri, 15 May 2026 20:12:53 GMT
WORKDIR /tmp
# Fri, 15 May 2026 20:13:08 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 15 May 2026 20:13:08 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 15 May 2026 20:13:08 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:6a2d07df495cc055bce0251fe801ee08db90750f52e43a555be5dfd8f5023783`  
		Last Modified: Fri, 08 May 2026 18:24:52 GMT  
		Size: 28.1 MB (28116165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7adf782900ff504a4c57f8b9cb8ea757d277bb3e9f2fd79c98c9f3a116b4322d`  
		Last Modified: Fri, 15 May 2026 20:13:25 GMT  
		Size: 54.3 MB (54272927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67d335a0692f5b1959401f2e61acfba38b7c44d1e4707d0a4698ef12b68d1eda`  
		Last Modified: Fri, 15 May 2026 20:13:25 GMT  
		Size: 69.7 MB (69722656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1bbce5dc2aa7a299db64d18caece840bed0979c597e446c0638d8ab9e9d9813`  
		Last Modified: Fri, 15 May 2026 20:13:23 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a8eb2201873a85bf597fb5ad4ca3ce9edbc06ccb75dd0a30ce497ccd59734b4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5258133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1356e9c2ffbb0b82bd8966209b2abaa2e13e92b0ed5ace900170a619ee54d410`

```dockerfile
```

-	Layers:
	-	`sha256:fab42d12419af55a999f4f2c9ca668e588d85df6302445cbd5a94a282bcdc784`  
		Last Modified: Fri, 15 May 2026 20:13:23 GMT  
		Size: 5.2 MB (5243613 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:724c290485712f26eb44becf9cdfec5ae7de2dc936ab3402d72debe7261ecb0d`  
		Last Modified: Fri, 15 May 2026 20:13:22 GMT  
		Size: 14.5 KB (14520 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:5366255e6d44fc28cb5b4a221db5fe238c64a1c897d7549c118d568a0fdac6b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.3 MB (160313639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be08f5bfa890e2c5182dc414e976330ac05d95f0c1eb6bc3ad63e25bff96f99a`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1777939200'
# Tue, 12 May 2026 21:46:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 12 May 2026 21:46:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 12 May 2026 21:46:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 21:46:26 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Tue, 12 May 2026 21:46:26 GMT
WORKDIR /tmp
# Fri, 15 May 2026 20:14:29 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 15 May 2026 20:14:30 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 15 May 2026 20:14:30 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:0e29ea7436ed4beb1c38bcfee44589407e49fc690669b42b35db33a9588e820a`  
		Last Modified: Fri, 08 May 2026 19:44:06 GMT  
		Size: 32.1 MB (32078453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f57a4137454cc0810d06042c272eb08276000e4b66a91f77145ef48d12c8463a`  
		Last Modified: Tue, 12 May 2026 21:47:32 GMT  
		Size: 52.7 MB (52669152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f196abc4fefe6f414e0100052dd8182945cf67cc7d015af36a673aa6fd6ae03a`  
		Last Modified: Fri, 15 May 2026 20:15:05 GMT  
		Size: 75.6 MB (75565387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa76b4e92f87697bbde2b3471a5b82e42e9638507b41cb52b8e8aa88b661c9be`  
		Last Modified: Fri, 15 May 2026 20:14:48 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:49938763c23e711b4b3bc275eeb667dcd627426958e459fc7c4061b93488125f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5257354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:665f4eb3d7f84588c571bc56fa588c4b671b4eeeba1f09d8f1c0cb3e72d4cef4`

```dockerfile
```

-	Layers:
	-	`sha256:25fe345f72019470a7263258c9493a12066f8010b4d61a56db6e19f84d6c89c8`  
		Last Modified: Fri, 15 May 2026 20:15:03 GMT  
		Size: 5.2 MB (5242905 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97f9339783c7a53719bb363682fc20cc2938023eba3b03dcd2d5eed2ca6da926`  
		Last Modified: Fri, 15 May 2026 20:15:03 GMT  
		Size: 14.4 KB (14449 bytes)  
		MIME: application/vnd.in-toto+json

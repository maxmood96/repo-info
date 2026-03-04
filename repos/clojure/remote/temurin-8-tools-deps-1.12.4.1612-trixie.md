## `clojure:temurin-8-tools-deps-1.12.4.1612-trixie`

```console
$ docker pull clojure@sha256:9a6565a2f82c501475c48484f4fb61c5f93fc75d76f823fb7afba5ccce2ba591
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-1.12.4.1612-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:9fc6bbe5600142df40f90f760a29fdd413a62e7766bc1391be7848fe642903dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.0 MB (190030914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c4fe85a197d202d4392d13df988087b41c51a3fafdf9e75d91655da68e38820`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Wed, 04 Mar 2026 17:49:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 04 Mar 2026 17:49:09 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 04 Mar 2026 17:49:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Mar 2026 17:49:09 GMT
ENV CLOJURE_VERSION=1.12.4.1612
# Wed, 04 Mar 2026 17:49:09 GMT
WORKDIR /tmp
# Wed, 04 Mar 2026 17:49:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "21d16fbce3e546c4f0163c78aba0eb0293993c7fa1aba77d089fdbfa445e38a2 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 04 Mar 2026 17:49:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 04 Mar 2026 17:49:26 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:866771c43bf5eb77362eeeb163c0c825e194c2806d0b697028434e3b9c02f59d`  
		Last Modified: Tue, 24 Feb 2026 18:43:22 GMT  
		Size: 49.3 MB (49293124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a34c42638a1da098774014b4b60a26b1383672dfaafcdc53985d66c99a13ddc4`  
		Last Modified: Wed, 04 Mar 2026 17:49:46 GMT  
		Size: 55.2 MB (55170110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24ecddfc88d893f7f5ba337507e69f146ec24218a7c7fb14ec2b79e89192e618`  
		Last Modified: Wed, 04 Mar 2026 17:49:46 GMT  
		Size: 85.6 MB (85567037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fda901d9f5b9b0f5216d4f415e9f440c944c8984f853692a7833b0063187306e`  
		Last Modified: Wed, 04 Mar 2026 17:49:43 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.4.1612-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:3f05ef6f413e65f4d5101331c8529c077837be2a6a7da362e84da82c01e22c41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7605750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecb5521de248e8c6635eb78cd47c282c962927c1d8130fabc186719eefda2cbd`

```dockerfile
```

-	Layers:
	-	`sha256:87f6d7b77cb13bbcad5ed1052bce08e17f4c0fe22ab65394d56a74d015dd63e8`  
		Last Modified: Wed, 04 Mar 2026 17:49:44 GMT  
		Size: 7.6 MB (7591580 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dcc3a35274a17b2e380fd39eb5cf0b26bb0510ae0fb6094c55f01075d8a77d7a`  
		Last Modified: Wed, 04 Mar 2026 17:49:43 GMT  
		Size: 14.2 KB (14170 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.4.1612-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:aab54106b4792172d69f417022635e2683f0fd7694ee226d9d9547632a5c713f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.3 MB (189287255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e42985103a05557fc011dca626cbb1c04c679834814c2472aeb17fb764ce7b3`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Wed, 04 Mar 2026 17:48:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 04 Mar 2026 17:48:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 04 Mar 2026 17:48:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Mar 2026 17:48:36 GMT
ENV CLOJURE_VERSION=1.12.4.1612
# Wed, 04 Mar 2026 17:48:36 GMT
WORKDIR /tmp
# Wed, 04 Mar 2026 17:48:55 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "21d16fbce3e546c4f0163c78aba0eb0293993c7fa1aba77d089fdbfa445e38a2 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 04 Mar 2026 17:48:55 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 04 Mar 2026 17:48:55 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:ac9148dc57ca750b09f3f3da6f16324e1a3b62432b2726734535ec610e1a9232`  
		Last Modified: Tue, 24 Feb 2026 18:42:56 GMT  
		Size: 49.7 MB (49652168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cf424ddfc041e368711e1442ca783a5c116042b991f16b46a83fad5e8ad73b1`  
		Last Modified: Wed, 04 Mar 2026 17:49:16 GMT  
		Size: 54.3 MB (54251614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ffdbaf4b2d19b30f524ea576713c723d1353b49e8f00857bd893825b387fa2e`  
		Last Modified: Wed, 04 Mar 2026 17:49:15 GMT  
		Size: 85.4 MB (85382826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd3860b80d0d400db1028ca5c2ce0b9baa853efef81c69cc4709640f9f310e69`  
		Last Modified: Wed, 04 Mar 2026 17:49:13 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.4.1612-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:5ac78dc02563360bba0194487675f29a9c2408634e70d81a01d333b302b5329f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7613598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7d5a81fb1ce1bd45e6fe1e7a6a6e9b7eba8f2d140d4ec91a3c4ba27168606ae`

```dockerfile
```

-	Layers:
	-	`sha256:abd9c83983059293ac937d2917302673f96ba2001dd5d1253a19e25909bf73f4`  
		Last Modified: Wed, 04 Mar 2026 17:49:13 GMT  
		Size: 7.6 MB (7599310 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd0fbf164e05950d39045fdca00e29f4036a448932f17eb1d25caf6d34a37bb1`  
		Last Modified: Wed, 04 Mar 2026 17:49:12 GMT  
		Size: 14.3 KB (14288 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.4.1612-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:7ffd1cfea04e85831dd45ca7ca11a75b42e8fa6e52692b68e1bcf633dda925a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.7 MB (196739398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2df95ca3bbe371618a4d3db5bd08f3a7e336b2d05d2f0874b63b8210b16d906`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1771804800'
# Wed, 04 Mar 2026 17:49:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 04 Mar 2026 17:49:49 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 04 Mar 2026 17:49:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Mar 2026 17:49:49 GMT
ENV CLOJURE_VERSION=1.12.4.1612
# Wed, 04 Mar 2026 17:49:50 GMT
WORKDIR /tmp
# Wed, 04 Mar 2026 17:50:38 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "21d16fbce3e546c4f0163c78aba0eb0293993c7fa1aba77d089fdbfa445e38a2 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 04 Mar 2026 17:50:40 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 04 Mar 2026 17:50:40 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:468eb7cd0e9ceb9e5b1c4c9daadd36c2fd1f1ee82c667dc1a7d70fa95600a20f`  
		Last Modified: Tue, 24 Feb 2026 18:45:11 GMT  
		Size: 53.1 MB (53112261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3006c18c8eefc56c675d719c87c3f5542132f775159b2d5bca8e54f5e6fedfe`  
		Last Modified: Wed, 04 Mar 2026 17:51:16 GMT  
		Size: 52.7 MB (52650390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74372a783e76ab319214b05cf3617ccfb817dd2c09afdd7b9611f62829eecda5`  
		Last Modified: Wed, 04 Mar 2026 17:51:17 GMT  
		Size: 91.0 MB (90976101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85fe4ec37f144bef93e8e00b57c3dcb70b48de9abc6f8f99cf3fe2eaffba602e`  
		Last Modified: Wed, 04 Mar 2026 17:51:14 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.4.1612-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:61ad9def5314e892066e118febd4a30dc2b30b776c530829c375d9c8dd2e495c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7610814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:562e7efad474fd05ee465b78d9f01bfd51342358378c5b7069bc7c14bb9f906c`

```dockerfile
```

-	Layers:
	-	`sha256:e0dd25a09658da503b8d35bce1783637bbe91c6c9ef5fb9873da03c71a30ff51`  
		Last Modified: Wed, 04 Mar 2026 17:51:14 GMT  
		Size: 7.6 MB (7596596 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29a23d25fb1024d98fc763efbd7de8ab100492432e32b33d6c47ad83f8762a4d`  
		Last Modified: Wed, 04 Mar 2026 17:51:14 GMT  
		Size: 14.2 KB (14218 bytes)  
		MIME: application/vnd.in-toto+json

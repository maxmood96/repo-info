## `clojure:temurin-21-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:0e3fd69b8ee0260848ede50908e1a90e1dd1ff71be74f69b511568aec6fae32f
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

### `clojure:temurin-21-tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:13ef3504bd060ca3d839256112d2ed76a3d6d51bd1e6c52928445cfcc41e2265
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.0 MB (253048423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:966e6874ad4cfd2a581f89f41fb8cfe0020e1dc7cc65a598145fd85e4623901b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 02:19:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:19:45 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:19:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:19:45 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Wed, 24 Jun 2026 02:19:45 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 02:20:00 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 24 Jun 2026 02:20:00 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 24 Jun 2026 02:20:00 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 24 Jun 2026 02:20:00 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jun 2026 02:20:00 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:68629629b516c3cd6f5e71ffbe18e32afb1ae5b4926c92d058c0f11ef1fd58a3`  
		Last Modified: Wed, 24 Jun 2026 00:27:52 GMT  
		Size: 28.2 MB (28237639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d2d1d869c49c3af02fef7c554f0665920d663e783beacb5817a4f0ffcc63503`  
		Last Modified: Wed, 24 Jun 2026 02:20:24 GMT  
		Size: 158.2 MB (158166945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8d759213525f3abe5be9737f34189e262e16728451e05419b65582f9660bf67`  
		Last Modified: Wed, 24 Jun 2026 02:20:23 GMT  
		Size: 66.6 MB (66642797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:026eb66d9aa35681bcba5fcb7119542676fdb812b3b4d55d1b70c44c92cfe8cf`  
		Last Modified: Wed, 24 Jun 2026 02:20:19 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9752cc0e20f494836a7c36261291c3f5679704b2c1233cf209228ba214bd4216`  
		Last Modified: Wed, 24 Jun 2026 02:20:19 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:4f83cf7b2fd8f63726637be13988911f6821c8da3cb509724e0aa1be6ca795b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5131841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29b0eb76e3458acf78233d47d469445e07e1b5c95504022d9fcaa9881b462e41`

```dockerfile
```

-	Layers:
	-	`sha256:679072371ffc5f6c4ba20f83673b5ec80de7d0844b7218ae1bf7513b5ca260ac`  
		Last Modified: Wed, 24 Jun 2026 02:20:20 GMT  
		Size: 5.1 MB (5115851 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fbca8815b4c5b1cef7310c9d9544afafcd18038696fff38bbc3ffc914b5f5c73`  
		Last Modified: Wed, 24 Jun 2026 02:20:19 GMT  
		Size: 16.0 KB (15990 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:fa17386eb3ea0742a20a345ec50152ffb822ad156334f88754888792d2b3680f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.2 MB (251228079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02c2feeed6a05169283c2fa7d6b78833290971f10783c87adce0ae2d935da3e3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 02:25:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:25:59 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:25:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:25:59 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Wed, 24 Jun 2026 02:25:59 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 02:26:13 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 24 Jun 2026 02:26:13 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 24 Jun 2026 02:26:13 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 24 Jun 2026 02:26:13 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jun 2026 02:26:13 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:74f1dcfcc9c80045f6f6394ffcfc261cb19d0c71b97e964aec3d4abf4e0f7009`  
		Last Modified: Wed, 24 Jun 2026 00:27:48 GMT  
		Size: 28.1 MB (28122418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f18aefff1f7a59c8b8b4356d25fee763811f17dc1e1a63105c46349ca6cc016`  
		Last Modified: Wed, 24 Jun 2026 02:26:36 GMT  
		Size: 156.5 MB (156461287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7677f6393d2fcf68745d01df274802f689057a9623d7cfaf47e5cedf72e200e1`  
		Last Modified: Wed, 24 Jun 2026 02:26:35 GMT  
		Size: 66.6 MB (66643333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc9478fef3d7f6958533dbceb681c7cef7526996f164a0c48eb855d844bd27bf`  
		Last Modified: Wed, 24 Jun 2026 02:26:32 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0409a60f51d8bd361d39df4f47110b10a0ed1c317a4afe71454b6e8889c4659`  
		Last Modified: Wed, 24 Jun 2026 02:26:32 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:31104b84cb9f157446bef4dd1b3bf4bb5e712e13ca75f5e0535233fcb76588ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5137720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fccb6615ca7b38d20669ed5ae0e51737f00e5c8f8cbb54e5ac3d53766baf61db`

```dockerfile
```

-	Layers:
	-	`sha256:d8f06591df0f27f650d006df265818f8bb7c403685bb7f19a81d1b1254596b4b`  
		Last Modified: Wed, 24 Jun 2026 02:26:32 GMT  
		Size: 5.1 MB (5121612 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16cb03a6de9ef3605597f079c2b46a9ab6cc1a370dfab0d42b5b98bdca991653`  
		Last Modified: Wed, 24 Jun 2026 02:26:31 GMT  
		Size: 16.1 KB (16108 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:e82268ee6c9066b44526cae829805adcbf0f66f82a4a75e3df485e1eae32d25f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.9 MB (262902360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04557f677983bdc7f174a21cef56f157b37b24b72e57b2e2cb6af08b994e2d67`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 08:11:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 08:11:45 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 08:11:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 08:11:45 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Wed, 24 Jun 2026 08:11:46 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 08:19:45 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 24 Jun 2026 08:19:45 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 24 Jun 2026 08:19:45 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 24 Jun 2026 08:19:45 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jun 2026 08:19:45 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:aca68162e30a6a797424ddae2250996b638d7dd3b09085b7da2b627f63083af5`  
		Last Modified: Wed, 24 Jun 2026 00:27:33 GMT  
		Size: 32.1 MB (32081978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d56a5a9576fb59a58c214f675faea6c921a30a0dc3a817cc0362e349d5c092ad`  
		Last Modified: Wed, 24 Jun 2026 08:14:59 GMT  
		Size: 158.3 MB (158343211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef136642e3791adefd196e1ca93ca099b36e1597a158b3dde6bc138887c5ebb4`  
		Last Modified: Wed, 24 Jun 2026 08:20:17 GMT  
		Size: 72.5 MB (72476130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec8b60ef65857c0b6a85cb350b01aac115d5052a6bcb00c99b27c4df8d8adb91`  
		Last Modified: Wed, 24 Jun 2026 08:20:15 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:463a99136395c4379e9c9dec4f508061faaa5ca52048c97f86bc7be87c5bef1f`  
		Last Modified: Wed, 24 Jun 2026 08:20:15 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:9b801ccbbe6a477f45239faae1e16169d711f0add4eda20d5892660f6391fc0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5137045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e08d27e540f4b3450b0dd3e02e30d3956f16976f9782237c6c1cf4f2c22d8fb6`

```dockerfile
```

-	Layers:
	-	`sha256:a2594946242db9e1e8eda27df86114cdcba8287f4fc7abd28f7f1f15eb924b29`  
		Last Modified: Wed, 24 Jun 2026 08:20:16 GMT  
		Size: 5.1 MB (5121009 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2da9842fe0e4b8799f2b1a3216be9771d5e5b40000c6d92a3713a72c67382c13`  
		Last Modified: Wed, 24 Jun 2026 08:20:15 GMT  
		Size: 16.0 KB (16036 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:b2cfb04878e6889946581b53e9b7c617669811d2f74c525a86cd914455a2e105
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.7 MB (239735372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:798c578bbaf236ca973637c05c9c97ae5dc0494b85fa1218bcccd75040f5c2ed`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 04:14:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 04:14:43 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 04:14:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 04:14:43 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Wed, 24 Jun 2026 04:14:43 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 04:16:49 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 24 Jun 2026 04:16:49 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 24 Jun 2026 04:16:49 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 24 Jun 2026 04:16:49 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jun 2026 04:16:49 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:e9aeeda7513dde59469463716e9e14f36210d6570c3cad5e5440b32d941733cd`  
		Last Modified: Wed, 24 Jun 2026 00:27:21 GMT  
		Size: 26.9 MB (26893585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5826e9d8424a8f27820a67c0c7ea6c7db06d965fa6dbb950d7b53496a99d834`  
		Last Modified: Wed, 24 Jun 2026 04:16:13 GMT  
		Size: 147.4 MB (147388430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca391df5e4c04205b2ed110593ae8cf0b105a63343f5aefb4de304e5d51acdc8`  
		Last Modified: Wed, 24 Jun 2026 04:17:13 GMT  
		Size: 65.5 MB (65452319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f68594d521d58f16b093ebd6417381d68cdf1baa18fdc1c68d910ee9b6d4741b`  
		Last Modified: Wed, 24 Jun 2026 04:17:11 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eac550c1b4faad97fea2e71f15dacb386e9a8c65318017944bc14fd816b1c3b`  
		Last Modified: Wed, 24 Jun 2026 04:17:11 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e0c14289c7590c2ba08bab8b7f8f065d8fa77733adcdc1d1287b2fbf897fd133
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5123161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6ab45abc5a7c7f66a55a24c79abebfe088a9ccf69ad9354ebb68e1cb69e8600`

```dockerfile
```

-	Layers:
	-	`sha256:b25b520c0f02111c2063bc332657840f17bb3dcfc4ecfb124548bc64933c7845`  
		Last Modified: Wed, 24 Jun 2026 04:17:12 GMT  
		Size: 5.1 MB (5107172 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05e2c1ed01900b79c2ee3860254a093d558f2d1e6f33bb0f9e5d6eb189c0c94b`  
		Last Modified: Wed, 24 Jun 2026 04:17:11 GMT  
		Size: 16.0 KB (15989 bytes)  
		MIME: application/vnd.in-toto+json

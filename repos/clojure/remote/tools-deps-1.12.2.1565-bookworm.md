## `clojure:tools-deps-1.12.2.1565-bookworm`

```console
$ docker pull clojure@sha256:03c935d7fb1e1c67f7b1eef506f712ff1ad42b85f4bfb9f67578fc1691892117
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

### `clojure:tools-deps-1.12.2.1565-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:39c8f64ba8a104e5ae4cb441aa38639492dcfde1276fa34d20100788fb10746f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.4 MB (287424008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:333339678130092110bb23c9d001fd90b08a2a0ddebbdb8633e7ec1a390c9ae0`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 26 Aug 2025 17:11:52 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1757289600'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:8fb375ec14f3df8b31b70d0216508565ab7264a7e16cac4f8cc07f8eca22445f`  
		Last Modified: Mon, 08 Sep 2025 21:12:37 GMT  
		Size: 48.5 MB (48480610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6b3a8cf4d1c8fa76c9eb090723efb4533874ea219c7950edbc0d4cb85900ac1`  
		Last Modified: Tue, 09 Sep 2025 01:50:04 GMT  
		Size: 157.8 MB (157804796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17bf3206203b83632fc471ba3fe0bed57b7e73e80b1e8f16b36271063b52fff3`  
		Last Modified: Tue, 09 Sep 2025 01:50:12 GMT  
		Size: 81.1 MB (81137564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c336c725bb0f06d756aa30dcf981b3c87290d7ab678c5f0837a6f1ee8a1ac27`  
		Last Modified: Mon, 08 Sep 2025 22:58:57 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0fdfdb9ed9f6ae5928ec285373b32d34afc549ee802134d90ff959b09e0b5f1`  
		Last Modified: Mon, 08 Sep 2025 22:58:57 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.2.1565-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:4932e78fcf9b82a62b2a0b1fd8f81de12b230df7b38742f96450da2d85c3e1c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7397812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a32457538e914c76aa76d2b06089255773805b5b71f5c1970d64a54738bb67d`

```dockerfile
```

-	Layers:
	-	`sha256:6f46718cf3988ee6b79ccc5c8396f12d7a064095765f308d900a72982f08361c`  
		Last Modified: Tue, 09 Sep 2025 00:39:45 GMT  
		Size: 7.4 MB (7379992 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0909125bc1124b41fda3e5abe0640d444ce9f24c1a61ffb29bca2d3330dce6a`  
		Last Modified: Tue, 09 Sep 2025 00:39:46 GMT  
		Size: 17.8 KB (17820 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.2.1565-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:2fb3895eb6e12ffa1acd788d81777fdc425172517b2856b45e54a23d6a32a57a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.5 MB (285467123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e151d18adfa2bde2f0400d287d676fdfed4131be10a7c455fd8dbd3c73491dc`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 26 Aug 2025 17:11:52 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1757289600'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:a9331b686701a987bcd276cc69a0f676d471ccda1aa353d2f7fad017f2894cd0`  
		Last Modified: Mon, 08 Sep 2025 21:14:32 GMT  
		Size: 48.4 MB (48359019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7d4ebfad27d387828fd2c785a6f5a5733e9c11de984d510197cc8e6e280a292`  
		Last Modified: Tue, 09 Sep 2025 05:01:40 GMT  
		Size: 156.1 MB (156081188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:131af69a301692d333a27ba51ce86c26da92fa799785627b7bee198cdc1a143f`  
		Last Modified: Tue, 09 Sep 2025 05:07:10 GMT  
		Size: 81.0 MB (81025876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae5b90ba88b915d5c1f637754880ba6c32c5749fecb5d13f4e0859a632b92e50`  
		Last Modified: Tue, 09 Sep 2025 01:18:05 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c09b24e8d97ee81e0ab827a225f59b5c0a1b755a4f4afaccbea78f54ae085ad7`  
		Last Modified: Tue, 09 Sep 2025 01:18:07 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.2.1565-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:03a74ce111a1d0e88552da9127123bc3107f0f24e5222e34435390076a762b24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7403037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84eeb27ff66a5e6c88d987a2946c418f42cdba294610801fd5048c43fdbea3b0`

```dockerfile
```

-	Layers:
	-	`sha256:1b4b99df4140c1b3933562eb8e3ffe36ff2e129d38f2bf54321a63b3aeaa2348`  
		Last Modified: Tue, 09 Sep 2025 03:39:28 GMT  
		Size: 7.4 MB (7385827 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4fefb57c97d6df72800e33001fe4335c894182ddff428eb73e85439c8e38e352`  
		Last Modified: Tue, 09 Sep 2025 03:39:29 GMT  
		Size: 17.2 KB (17210 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.2.1565-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:bf197ef82c780179c101ef4cd5c4584bf5d28e72b8a0b7f40a34b4aa58bd3d90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.3 MB (297269991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49fc6c6ca042e810232a770ab5732e4f17503057e28f4d04f5ced4d71402ceba`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 26 Aug 2025 17:11:52 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1757289600'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:64b8116dd43c29a2a4aa3131cb4895af0a7267cc5883e3761556e54c369be9af`  
		Last Modified: Mon, 08 Sep 2025 21:22:08 GMT  
		Size: 52.3 MB (52326822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19b2ca9ff1a3fccb012f6c51a9f097c6995575e5e55d69deb7d54ac91943ca62`  
		Last Modified: Tue, 09 Sep 2025 09:35:24 GMT  
		Size: 158.0 MB (157963479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7e7c06ab10268aa1b3a5b8bf2361a696eab5af497e9f07984499aa47c75051a`  
		Last Modified: Tue, 09 Sep 2025 12:47:15 GMT  
		Size: 87.0 MB (86978647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72562ecbedd2159dab4f3a7fb2e042d9b0371816114d7d11f802fb5f2b2061aa`  
		Last Modified: Tue, 09 Sep 2025 12:46:47 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f3bea5687d96efa572766e2b400297890d013020145d00dcfa8057ea981b16c`  
		Last Modified: Tue, 09 Sep 2025 12:46:47 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.2.1565-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:c77b2a7eccdf24b927e77008998c3b3b5be4f2a8d2d509ac216839e00d72c576
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7403146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d41b4517a074ab3dbd411ca442453c0e1b898552821543e4bc578eb6112fb418`

```dockerfile
```

-	Layers:
	-	`sha256:6bfc6ef18d380480945e61752acfebb3d38e5112be3c984a2a21996c45257900`  
		Last Modified: Tue, 09 Sep 2025 15:37:53 GMT  
		Size: 7.4 MB (7385242 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa58a8bea5ffd35098afce9ba32a53eca385b8ec034de3aed5bfcfe61728199f`  
		Last Modified: Tue, 09 Sep 2025 15:37:54 GMT  
		Size: 17.9 KB (17904 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.2.1565-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:d2a05f41f0a126adc2683e08262fb577a9bea7dde20d593037ef416efc23ed48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.1 MB (274116628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c44803c4ca511e23ffcc3d92075995d9e2f6c9c0711321cfdf8668875f85458`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 26 Aug 2025 17:11:52 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1757289600'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:67e2d91fae4fd9af13e4e364bf8120dcca7856e8273995cc0651acae70b27e8e`  
		Last Modified: Mon, 08 Sep 2025 21:18:01 GMT  
		Size: 47.1 MB (47137539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84772536e34edd89b294c09dbe86293a053e24f7d3644f8bc0e4612df16f4795`  
		Last Modified: Tue, 09 Sep 2025 07:01:48 GMT  
		Size: 147.0 MB (147027040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29133b04619850b73aaf96e5c487efa0101ef16ad9027c451a7eb55edb17ef5a`  
		Last Modified: Tue, 09 Sep 2025 07:01:56 GMT  
		Size: 80.0 MB (79951012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff869e9132e80d33c1702964ab61924520ba2ab04a92be0f4e514cc80156ab5c`  
		Last Modified: Tue, 09 Sep 2025 06:15:32 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57847003d583d69303f6961da0ef43ae141156d9713375deeb503c450f7de786`  
		Last Modified: Tue, 09 Sep 2025 06:15:37 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.2.1565-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:8474c4a9e45dab4c50daeab0fb9374b4c67b314b2eed6e1fca15eb843a2b9a5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7389132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec61a9f71d0f1f15d49fcb9055415bef994dfb61802a7acf6b3f4aa6e9f2a1b2`

```dockerfile
```

-	Layers:
	-	`sha256:7887b5bc0d9ea87ab1c4226f861a7119be9e3794c042b395313f6969ccc21437`  
		Last Modified: Tue, 09 Sep 2025 06:38:18 GMT  
		Size: 7.4 MB (7371311 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36e3caf7def50115fb23a08cefcb8ae296dc1d6f2f480226cba0d3a094816527`  
		Last Modified: Tue, 09 Sep 2025 06:38:19 GMT  
		Size: 17.8 KB (17821 bytes)  
		MIME: application/vnd.in-toto+json

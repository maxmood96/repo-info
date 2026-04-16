## `clojure:temurin-17-tools-deps-1.12.4.1618-bookworm`

```console
$ docker pull clojure@sha256:f1178f3b3b8ad525b0238009756af294fdb6df79160580da33a4d0917732313c
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

### `clojure:temurin-17-tools-deps-1.12.4.1618-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:0b10f255493b28a033eebcd87f3befc1e35a7fb879f5fdafe03ae4abbc5582c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.3 MB (275285179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51be4d9939d7aa4ca3f63dfbeae2e0c247310ececa5ca9ec6a62b9c8b30dc25f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1775433600'
# Wed, 15 Apr 2026 22:04:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 22:04:02 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 22:04:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:04:02 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 15 Apr 2026 22:04:02 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:04:17 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 15 Apr 2026 22:04:17 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 15 Apr 2026 22:04:17 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 15 Apr 2026 22:04:17 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 15 Apr 2026 22:04:17 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c150dd3f5fc91eabd1818cc30298a4a956782621583cadfd369c4d327584008e`  
		Last Modified: Tue, 07 Apr 2026 00:10:26 GMT  
		Size: 48.5 MB (48488823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:743be0e1a74c449b8e6dd7c5721bd5585aaee7bc4aa161f78729828ce86c2217`  
		Last Modified: Wed, 15 Apr 2026 22:04:39 GMT  
		Size: 145.6 MB (145628750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:592a139358ff8881c217684c9b4b4476e9735e686be4b534652720d79aa4197e`  
		Last Modified: Wed, 15 Apr 2026 22:04:41 GMT  
		Size: 81.2 MB (81166564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a6fa0ea72920f4ac89cc5a8aac3a9b115fb28d4048ce8b06f74046335416dfe`  
		Last Modified: Wed, 15 Apr 2026 22:04:37 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fd6026ec4063da3dae96f4428310945d52b18a686af0928041edb1cf468c9f4`  
		Last Modified: Wed, 15 Apr 2026 22:04:37 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1618-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:317c8e3273ebd88404faca6148975e0ec7dc2d4b7669cf07c815f451c8a460e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7394080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4110e9691cd337912627f05fd33fd6ad3f7a392c383439eb4c9630d8565ee2e`

```dockerfile
```

-	Layers:
	-	`sha256:4145863a91f2fc69834d6f718032d4a41e8b3ec9785fa23fa175f27eaa926af0`  
		Last Modified: Wed, 15 Apr 2026 22:04:37 GMT  
		Size: 7.4 MB (7378302 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2319b2436c6ee8612541fd4f1d1ac466d02762b907a0e41491a698f0263eeea`  
		Last Modified: Wed, 15 Apr 2026 22:04:36 GMT  
		Size: 15.8 KB (15778 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.4.1618-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:d7c7eb2e6a372215bf3a95c874efd972db7057ce8ca7524f261d0631dff4680c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.0 MB (273982616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5735d36d4307bbe70f0c6764bd0a983ffd4bdc89a880b06405522c8f937af71`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1775433600'
# Wed, 15 Apr 2026 22:15:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 22:15:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 22:15:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:15:25 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 15 Apr 2026 22:15:25 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:15:41 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 15 Apr 2026 22:15:41 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 15 Apr 2026 22:15:41 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 15 Apr 2026 22:15:41 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 15 Apr 2026 22:15:41 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:d03e31a3f7ef0d2866d799846c3a18286fab6fcddbd8c523f3cb5ed1bd2f31a3`  
		Last Modified: Tue, 07 Apr 2026 00:10:26 GMT  
		Size: 48.4 MB (48373262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2daf774e2bcce628ade6fa3bf20ccac0d1bbb68755087ac7df20f671e73f0a9a`  
		Last Modified: Wed, 15 Apr 2026 22:16:07 GMT  
		Size: 144.4 MB (144436243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46084e3a5283e2aeee36edcd8ce9b81462e4d1ce36198613b6e72f15ee77b895`  
		Last Modified: Wed, 15 Apr 2026 22:16:05 GMT  
		Size: 81.2 MB (81172068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:601a4d0ffa610bff57250ac7313e331212cb3d086a60b247ae87d528784e231b`  
		Last Modified: Wed, 15 Apr 2026 22:16:01 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58709f0190bbeecadff08da32bac3e54a8413e5b842d3b33ad9fa84392fe644c`  
		Last Modified: Wed, 15 Apr 2026 22:16:02 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1618-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:cd1bf05409bffe5f38d0f988fc4f26261f052b64ee8f3a5e90250c55110eb204
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7399961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c84c3175d1ba08828afc9059b486b296ea7458a04963c7aedb663880d05c87b0`

```dockerfile
```

-	Layers:
	-	`sha256:fd38448a53d75bf229e0e62b8fbbd4ed9e90ad1626eb58d925c9fe35ab3c700a`  
		Last Modified: Wed, 15 Apr 2026 22:16:02 GMT  
		Size: 7.4 MB (7384065 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db3deef1a20c28c9b27a6f75411f6a36b36e113d9ce8911f37aeff59e398cffa`  
		Last Modified: Wed, 15 Apr 2026 22:16:01 GMT  
		Size: 15.9 KB (15896 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.4.1618-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:8f8875b343a78011f1ef98cae353826906e2def01499332ef2a338b2574a47a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.8 MB (284780536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a7006564f520fb21c04233d4ca3fbffbab8df5113a53e5ceb76ae916cf2494a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1775433600'
# Thu, 16 Apr 2026 02:49:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Apr 2026 02:49:05 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 16 Apr 2026 02:49:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2026 02:49:05 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Thu, 16 Apr 2026 02:49:07 GMT
WORKDIR /tmp
# Thu, 16 Apr 2026 02:54:24 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 16 Apr 2026 02:54:25 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 16 Apr 2026 02:54:25 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 16 Apr 2026 02:54:25 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 16 Apr 2026 02:54:25 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6b775f7ad22043f8bb75d535d8a1279e43453a08a4a9e6a0b48c020c9b387079`  
		Last Modified: Tue, 07 Apr 2026 00:09:43 GMT  
		Size: 52.3 MB (52336938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25284de88594517d85a7360eef895de970f33043b86caf252b64664918c3e557`  
		Last Modified: Thu, 16 Apr 2026 02:50:31 GMT  
		Size: 145.4 MB (145438294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f13b6d39cb9bdb1b333864816de7d057050d81a654f577c18cc3f7bc905a94a`  
		Last Modified: Thu, 16 Apr 2026 02:55:08 GMT  
		Size: 87.0 MB (87004259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6da97750b4474f32873d40a42edf8f16e673d6c146689ed8001604f71fe9dbc`  
		Last Modified: Thu, 16 Apr 2026 02:55:05 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ce9273f10bc056901c484965125ab10fd2a2db64ce330d93c2326343dc2e647`  
		Last Modified: Thu, 16 Apr 2026 02:55:02 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1618-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:8948b02b2fe445ce60b7a01c243ed48c2d2b2dbf848d0debd568998c9b72091f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7399344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1697f6799032f114f6911d6bcc86073c1489952e7bc17b6f6cf3e148c5a36a3`

```dockerfile
```

-	Layers:
	-	`sha256:36394c18e098c6630ec748a9111af6f4bf17abc2a21f954bffb3d4336141a45e`  
		Last Modified: Thu, 16 Apr 2026 02:55:06 GMT  
		Size: 7.4 MB (7383518 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86b3fc1ec23a5f010f4304bd1f947bfa3dbdb5c7383e1e9115a162c07a6e8a9a`  
		Last Modified: Thu, 16 Apr 2026 02:55:05 GMT  
		Size: 15.8 KB (15826 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.4.1618-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:32df1e63c2ac49acbccd0da4d9001cdfa3902720d6cb9b1b39f183cd908cc8da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.8 MB (262755958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d6d59fbde8d5ff84e0d4577d95d469b6dbe6323b1257363051f87d9275f28ed`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1775433600'
# Thu, 16 Apr 2026 00:39:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Apr 2026 00:39:03 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 16 Apr 2026 00:39:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2026 00:39:03 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Thu, 16 Apr 2026 00:39:03 GMT
WORKDIR /tmp
# Thu, 16 Apr 2026 00:39:17 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 16 Apr 2026 00:39:17 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 16 Apr 2026 00:39:17 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 16 Apr 2026 00:39:17 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 16 Apr 2026 00:39:17 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:40ecbf1d4e17f6b072e6cef463823baec601d9f21c9dc33d98bd258448a986f6`  
		Last Modified: Tue, 07 Apr 2026 00:10:32 GMT  
		Size: 47.1 MB (47148084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b8384ac3b00a8a528a1ff7086fd4df80e77338dfe40e6b14a27fe5d14fb9615`  
		Last Modified: Thu, 16 Apr 2026 00:39:48 GMT  
		Size: 135.6 MB (135627011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fec1ea484c2da7f47f8ba99dca686cc02b7ef59cd0ee2d59ba9408863abae818`  
		Last Modified: Thu, 16 Apr 2026 00:39:46 GMT  
		Size: 80.0 MB (79979819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:651838aaedee847e6038c7904e757fbe18341c96b32e8fdb29ab5da508112c9f`  
		Last Modified: Thu, 16 Apr 2026 00:39:44 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ab4628c51f89706afe5f2ebcac50a234340f7e24ffaebbd019e8fda4fd7ffc3`  
		Last Modified: Thu, 16 Apr 2026 00:39:44 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1618-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:819c52b2f31d0ab591857f23e052ce52209a6268ea056fe1dbf27d8d3b3dcd83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7385399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51c6f2a435d3c36b86c2501dad03acadccf15fada7298275e4a203c06c7cbdae`

```dockerfile
```

-	Layers:
	-	`sha256:cdff4d4b4a02ccf5736e2539320aefd094eb3cc309f96761c7321a34d91dac62`  
		Last Modified: Thu, 16 Apr 2026 00:39:45 GMT  
		Size: 7.4 MB (7369621 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57b8bc7d043d048a4817c7f0b7340ff1602ed86dc002393457fa1f098e3a4235`  
		Last Modified: Thu, 16 Apr 2026 00:39:44 GMT  
		Size: 15.8 KB (15778 bytes)  
		MIME: application/vnd.in-toto+json

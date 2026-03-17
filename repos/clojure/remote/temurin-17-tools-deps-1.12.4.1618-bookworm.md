## `clojure:temurin-17-tools-deps-1.12.4.1618-bookworm`

```console
$ docker pull clojure@sha256:86f96fc82037f09434f4baee6db61cdce092031af0c3149cab7ee67ccf9c3bc2
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
$ docker pull clojure@sha256:33ceba3e66400140396db9952f0c28d3a7741fd84c035247d8c127685fd04b07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.3 MB (275295623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15f7d50480403d88ce2a866e22f7da0899a66dcd21dbb8f3ec3128039da0116d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 02:57:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 02:57:40 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 02:57:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:57:40 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 17 Mar 2026 02:57:40 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 02:58:32 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Mar 2026 02:58:32 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Mar 2026 02:58:32 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Mar 2026 02:58:32 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Mar 2026 02:58:32 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:9d2f29087bcd6d99efd909a99095549425cd63e27c71b3bf37f108c6b7c370f9`  
		Last Modified: Mon, 16 Mar 2026 21:52:42 GMT  
		Size: 48.5 MB (48488584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87ff8b0b9d4c1a2f510cecdd760da6095cf78c80f085e00a01311da4e729f02c`  
		Last Modified: Tue, 17 Mar 2026 02:58:12 GMT  
		Size: 145.6 MB (145628435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12fb6ad7dc43a3ba47a4f0b306f72d5d48c67d21b6789019a08af6f09c011ca6`  
		Last Modified: Tue, 17 Mar 2026 02:58:48 GMT  
		Size: 81.2 MB (81177565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c28152e97c5ba8b59af178d01191ba0a5de8e9da81283d94ded59c2f998ef73f`  
		Last Modified: Tue, 17 Mar 2026 02:58:46 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0323583ad3a6da6588ad0d075d061593c84c49f0f92ce4996a748bae0d9468f`  
		Last Modified: Tue, 17 Mar 2026 02:58:46 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1618-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:b9f0b6fee4aedde548163b842b33f4e62805a66bbce4043c8c5bf166c918d6c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7394080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6f11b102b41a157d6e8cdd182eab30b54d09554ccebddc6d8d4b3f34d727d2d`

```dockerfile
```

-	Layers:
	-	`sha256:983ed6cfc327230716663d693866fa801ef99102c9f8b11acf909ab219c38ae7`  
		Last Modified: Tue, 17 Mar 2026 02:58:47 GMT  
		Size: 7.4 MB (7378302 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d997d454c6cf67d2388fe8b32a72f6a02bc8d9ef0b5b12519c6c0bae38f623ee`  
		Last Modified: Tue, 17 Mar 2026 02:58:46 GMT  
		Size: 15.8 KB (15778 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.4.1618-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:9b3a5258349c3f1033e865ccb017230bbba1dfa96a17697f728cbe7d4d52249f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.0 MB (273968657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd49c6b142b0cf75f7183c9dd7ade0ec188e2f840dca4bb58be0cd2c6ac01d68`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 03:03:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 03:03:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 03:03:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 03:03:08 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 17 Mar 2026 03:03:08 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 03:03:24 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Mar 2026 03:03:24 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Mar 2026 03:03:24 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Mar 2026 03:03:24 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Mar 2026 03:03:24 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:2ea98bb5eec9d02a0d7b59638c683db4e1e749f998a317bc731e9506f8480b12`  
		Last Modified: Mon, 16 Mar 2026 21:52:02 GMT  
		Size: 48.4 MB (48373032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20722c105ddf91f1823079898cb9861547e1097f2f7e25349d03526ed289b3b7`  
		Last Modified: Tue, 17 Mar 2026 03:04:11 GMT  
		Size: 144.4 MB (144436241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b760beea9030c395f704364f33be3d7bfe31f9ac5f85de681675f1ba04479a5`  
		Last Modified: Tue, 17 Mar 2026 03:04:03 GMT  
		Size: 81.2 MB (81158345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c00798b77f8ec01218dfc3053702037110ac5fd538127908bf47355dcd0f6933`  
		Last Modified: Tue, 17 Mar 2026 03:03:48 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e49d99f0c149be11fdfd9d442df8cce038e28d250d58cda396243d78ae963fc`  
		Last Modified: Tue, 17 Mar 2026 03:03:48 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1618-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:cd30cc75aab0e9773cd08b9b4b87c5ed691195f634c7e5c4b41550248862414e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7399961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07f6c42136741f1bb2c1e80078689727c216a81d32b89086ef1022f515be810d`

```dockerfile
```

-	Layers:
	-	`sha256:5b316c43acfa61d9de10ace73ef26c76fefac7d5f0956349944404ab849e66b6`  
		Last Modified: Tue, 17 Mar 2026 03:03:49 GMT  
		Size: 7.4 MB (7384065 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:600e10e48d42d5b973ddc546f227f8daa587f14d830ed9e02c2ab6eb13e6c487`  
		Last Modified: Tue, 17 Mar 2026 03:03:48 GMT  
		Size: 15.9 KB (15896 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.4.1618-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:b58db38cb4275cc283daa6aeb32f21573afe857d136ac02b5571a2096c8faf09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.8 MB (284776015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1049bee248abe681aba87b419861a6da70ba6db2a3c02e9175733c374ddbe5de`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 18:24:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 18:24:37 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 18:24:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 18:24:37 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 17 Mar 2026 18:24:37 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 18:30:17 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Mar 2026 18:30:17 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Mar 2026 18:30:17 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Mar 2026 18:30:17 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Mar 2026 18:30:17 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c072e92b832614e86d956c6381c6b7617944feae3193ea5691e9506870844136`  
		Last Modified: Mon, 16 Mar 2026 21:51:19 GMT  
		Size: 52.3 MB (52336698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0ee64ed0afeae873fd2f06096ddec7906316112c3693f7c534e02be26621b37`  
		Last Modified: Tue, 17 Mar 2026 18:25:57 GMT  
		Size: 145.4 MB (145438236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddc3621686d4d4130cc10a6034d7a29a7ac3ebf82d6e3c02fce07e1c8477c04e`  
		Last Modified: Tue, 17 Mar 2026 18:31:01 GMT  
		Size: 87.0 MB (87000042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1db6b7fac07fec680ca092b5be38f1d8b2374f355e66445f9da98cf57505b4c`  
		Last Modified: Tue, 17 Mar 2026 18:30:54 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f562593312ad2a3a137ba4daba01aa5abe410fafcea2686e6069e54c6e5240d`  
		Last Modified: Tue, 17 Mar 2026 18:30:54 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1618-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:e02c700d8a570a003384471a532656451c0e456db201cfccd45acf2bf030baa2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7399344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:886fbd23342622a9184ad1a15593d65235e682869b1e802e4557effc743e2c2e`

```dockerfile
```

-	Layers:
	-	`sha256:4bfd444d8e0c99348c157544462180cc88e5bc02b38efd25f9e92728ecea2479`  
		Last Modified: Tue, 17 Mar 2026 18:30:59 GMT  
		Size: 7.4 MB (7383518 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b8ce5b92ae902badd96b49dbbc724ca5d2821c803005901e6eca4f407a4442a`  
		Last Modified: Tue, 17 Mar 2026 18:30:58 GMT  
		Size: 15.8 KB (15826 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.4.1618-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:51d8311a524f4960ab83cb78bbed9ba267aaef4dd758e70ece941deb8b022da1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.8 MB (262764768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:632a5536ac60af632147da9465eec0bf48f9bb5c4cc7e59e9fe9200ed64fed81`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 11:35:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 11:35:56 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 11:35:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 11:35:56 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 17 Mar 2026 11:35:56 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 11:36:37 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Mar 2026 11:36:54 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Mar 2026 11:36:54 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Mar 2026 11:36:54 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Mar 2026 11:36:54 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:7dbc3949555449666cc7651209b926019d3fc7f1511f7ebcd8979762b12d59c1`  
		Last Modified: Mon, 16 Mar 2026 21:51:27 GMT  
		Size: 47.1 MB (47147919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd40a19d3fdd28306df2092d2c8fa671adfcdd3151eda8f2cb8af27ef3517d5c`  
		Last Modified: Tue, 17 Mar 2026 11:37:44 GMT  
		Size: 135.6 MB (135626828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f55fe81085e53f5e00dd85a0c7c2469f49eb5e55224831142a0b17e42508502`  
		Last Modified: Tue, 17 Mar 2026 11:37:42 GMT  
		Size: 80.0 MB (79988978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70f2517b73ec14fba9826ae83adc81feb66828bd96b91880e059babdf315bf2e`  
		Last Modified: Tue, 17 Mar 2026 11:37:39 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d77f8bc723834aaa6c469e9efebac42a27940dbf98c38ffc3c8584e48f337a81`  
		Last Modified: Tue, 17 Mar 2026 11:37:39 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1618-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:0fed4d06f4a78b5a25b0606a3fde3f1e40057510183e4d229fa456e4523ce8af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7385399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e170fbb520e96431affe729ef249e0febd82eb706b4aee459d818e4ddbc5748`

```dockerfile
```

-	Layers:
	-	`sha256:c9ae3cfd8b8994941f6338b8dcf6207164b4b26a3a3c05256b0a3dbbd3109c1b`  
		Last Modified: Tue, 17 Mar 2026 11:37:40 GMT  
		Size: 7.4 MB (7369621 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cdd13b8e454c4a7b57f713b3298eb0405a6dc959a826c7e7b8808154fc18075f`  
		Last Modified: Tue, 17 Mar 2026 11:37:39 GMT  
		Size: 15.8 KB (15778 bytes)  
		MIME: application/vnd.in-toto+json

## `clojure:temurin-24-trixie`

```console
$ docker pull clojure@sha256:e213292c0df47db767bd6f10081a3850cf33af404c81e2c3c55381f349a631b3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:temurin-24-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:a7fb172344b1cff5bbf97f9309f8643017fba5bc32698299671fbd61a4f43088
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.4 MB (227422673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6136b1f4ed917593b9cf0f0a7494bc94038c5e7df368029d3bd1bb673591fb1`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b8364400c35b20e530ea76455b7a73bf615b17d9d6734e0c2539034d9fe0bed1`  
		Last Modified: Wed, 21 May 2025 22:28:00 GMT  
		Size: 49.2 MB (49246908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89f8f138bedeec141ce3d55ce0b45f1201bf4586387cff12a9796b55a032bbf8`  
		Last Modified: Tue, 03 Jun 2025 05:17:08 GMT  
		Size: 90.0 MB (89952019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4e738ca0291c9237a916711717d6e8bc714e3d1a4e4515a59c73ac7b6564835`  
		Last Modified: Tue, 03 Jun 2025 05:17:07 GMT  
		Size: 88.2 MB (88222708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40f6c8b8cef156ded1a8319e2f5c44cd6b50b5ec21d85811d10dd7303196e35e`  
		Last Modified: Tue, 03 Jun 2025 05:17:05 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccb27a1147660d6fa3320d0cee5fbe6f62a68c9084886a6f3e1853e277f63cc7`  
		Last Modified: Tue, 03 Jun 2025 05:17:05 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:4b4d1d594d579dde1af876c098b98d7fe17e64b65d7cf7a079a138bb68696a3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7284851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b7e43498fb15be1d231c991720e03083a676ee7822d6ff83469019061b0e23e`

```dockerfile
```

-	Layers:
	-	`sha256:d6ed041a9e4dadbc5544dbad36b599c61610b260c6c3b52e2852a1a223b2d946`  
		Last Modified: Tue, 03 Jun 2025 05:17:05 GMT  
		Size: 7.3 MB (7269062 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7a0fd86ebf0a8757bdcabd1bb00493d7a47a712c226686931a93b6dad9fbba1`  
		Last Modified: Tue, 03 Jun 2025 05:17:05 GMT  
		Size: 15.8 KB (15789 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:46e666eb6bbc8e38ee893ee790a3807c89e3eb7cf42712752d83e95553931c81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.9 MB (223885891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5544020075e1db0850b9a7dc6787fdbef57424343cfcea6e3e7ef94316607fb`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:397826b9fe635f12caff1a603eb12c37426a5b3dc563e0adff2debff0c68a6b0`  
		Last Modified: Wed, 21 May 2025 22:31:07 GMT  
		Size: 49.6 MB (49618294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcd679165a19bb68b3f7b7763bba4e4b86803022a4aa5c012a793f16e9893a08`  
		Last Modified: Thu, 22 May 2025 08:42:16 GMT  
		Size: 89.1 MB (89091185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffdd52f40fcb680b210d1a408176b7209b5a2327d22f779edf89367cfa1219a0`  
		Last Modified: Thu, 22 May 2025 08:46:51 GMT  
		Size: 85.2 MB (85175371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b17eb030e1682d3c4be6cacd8ce68ec863a9a11aed1dc1bb96a833844b6312bc`  
		Last Modified: Thu, 22 May 2025 08:46:48 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:655992ec9708e671c3da57b8095c23d6a9ab43475aed0e576b62ced71ae3de0f`  
		Last Modified: Thu, 22 May 2025 08:46:49 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:fab53cbafc102b79eb90f75904cd808407211b54c57602780008d5193d01f8f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7291997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0a6b2c4ea2e82404fb62df8ff12876615ffb9fc3e8d90f72e0ebccfbe071d89`

```dockerfile
```

-	Layers:
	-	`sha256:46c81913554ee22c3ce4ef2598776b4e33b79b7a1605f467a3c6720e4a5c5967`  
		Last Modified: Thu, 22 May 2025 08:46:49 GMT  
		Size: 7.3 MB (7276089 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:857f9164812b66f71a1c7d4acf2b0c8315a42b7e98bcf7528c967ac20967a420`  
		Last Modified: Thu, 22 May 2025 08:46:48 GMT  
		Size: 15.9 KB (15908 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:76b946a0ac56b30fe8f488300574b6b46294eaf9d28ad747cd76168c025c748a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.8 MB (233753653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a12a1f06df71f71e4f6e14e078caa3960c2a357ec504231b57de22a9bcbf3120`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:25dfffa4126a91eb76c700c90bfdc9a9e15f34c7438a81f16c8a6999bbde6e45`  
		Last Modified: Wed, 21 May 2025 22:32:01 GMT  
		Size: 53.1 MB (53080544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ebfbd0868423d13aa33ba10ef69806894afdc61ee1d350dffd794506757ecd6`  
		Last Modified: Thu, 22 May 2025 11:45:19 GMT  
		Size: 89.9 MB (89920243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eb6bb6acbdc3b35bdf5388c8e4c573bf729c28dfc1960e76a04570a8ebb395f`  
		Last Modified: Thu, 22 May 2025 11:52:14 GMT  
		Size: 90.8 MB (90751825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af348b4cdc2a25caf659a214efe622338a301e5d4e3f389a7a1917173a8eda1c`  
		Last Modified: Thu, 22 May 2025 11:52:11 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47f00d524333af5a62dd3e44326af73d2cf88257380c1af0d386ec6fdc4c6cdd`  
		Last Modified: Thu, 22 May 2025 11:52:11 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:23f2975cc0413caa6cd7e70af42d72cb65d0b0e717ecea8433a9588b8d50eff3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7290614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b506fb79678638898922a4ac5a15c6eb8f75ed9f1af5ee163d784adf1399915f`

```dockerfile
```

-	Layers:
	-	`sha256:3ebd6723879e36a2cd2e867d5dbe464e8be6d79a6d56d8f9ceef264055f38704`  
		Last Modified: Thu, 22 May 2025 11:52:12 GMT  
		Size: 7.3 MB (7274777 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5bca41298987a9ea3615401674f56004d18866f37d6c6cde9e534ab4f3afc2fd`  
		Last Modified: Thu, 22 May 2025 11:52:11 GMT  
		Size: 15.8 KB (15837 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:3b389ce51e14da1f98df0c08da083fa40411b5d5b79a0e424d75ced938386aea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.6 MB (219575420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e111178da8c925ce300a4ab6f1ae6ef41b3087a7fcc2a7547b05394e72856ca`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c83c5fa20952cc8610d790073e97537e7832127593042fa9c620fa910fe6f6b9`  
		Last Modified: Wed, 21 May 2025 22:36:51 GMT  
		Size: 47.7 MB (47731411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a66e0017b5778e4bade9bef89ef92a010b6f5851fad922be6870b59cdc2a453`  
		Last Modified: Thu, 22 May 2025 00:40:53 GMT  
		Size: 87.6 MB (87622251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68ad83b972f3e73c0c1927aaf6372ee6384833189cd3e48c09a402b4637bc7e5`  
		Last Modified: Thu, 22 May 2025 00:55:43 GMT  
		Size: 84.2 MB (84220717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b209cc370d26cb5333d5a1a897e14b2b03102ed08172e738a8c79344ac4532aa`  
		Last Modified: Thu, 22 May 2025 00:55:31 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f984b776eb492224d8a03bba8bd84b1d149cdbff8a44bafd453d827c91f0320e`  
		Last Modified: Thu, 22 May 2025 00:55:31 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:191bd61830ee26ab9a10780841f5cdd540e24ebb8d6f5f2fa228634d3992806c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7272808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ec413e1a96b8b4ce6d689cfe4d201b42009542199654a78cbfe2bf28c7ddb73`

```dockerfile
```

-	Layers:
	-	`sha256:2995afe46dff641d4803d95916536c7ba2422d25015b6f6bf3b6f0eb53ba9e3e`  
		Last Modified: Thu, 22 May 2025 00:55:32 GMT  
		Size: 7.3 MB (7256970 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55d0805cec474bf5ed4e6e7159bc7d3a1b6ef4fd5e0a9ea1a57009e790253a3d`  
		Last Modified: Thu, 22 May 2025 00:55:30 GMT  
		Size: 15.8 KB (15838 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:a4276601a6b15d753cb3cdc7ea64ff4df636c35c3327edba9aeace3cd43f8ab8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.9 MB (220880336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da7244fa66b498482b905364d1accc0572e00309fe68a8df27a52462d4fe7319`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:71c8524b25c34592c256fbae9045d0ade48f5e9889d37c5b2190092fa9017d48`  
		Last Modified: Wed, 21 May 2025 22:31:46 GMT  
		Size: 49.3 MB (49322227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13f38a21a13def6964dc50483f08faedaade5738b51a584056cc7447506d8a27`  
		Last Modified: Thu, 22 May 2025 04:07:53 GMT  
		Size: 85.2 MB (85216727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5917408d205dbd94f53ea805749e4503d3b45690f0677c746777aaa04baae063`  
		Last Modified: Thu, 22 May 2025 04:11:47 GMT  
		Size: 86.3 MB (86340346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:284d1aa4a746b1e55875b796e6e11a09db50ea3a4857efbae1924987ffacbbd7`  
		Last Modified: Thu, 22 May 2025 04:11:45 GMT  
		Size: 609.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b47910af6a1d915edf9b7536709600fd9f05b6a1c79ac6e5f74b82d8577436fa`  
		Last Modified: Thu, 22 May 2025 04:11:45 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:e7c774522a4407c4b412b72ff1b7abf153bd9f315c7417adcae0041c6782b006
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7283322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45a1ca141e89b2ca3caf2ffd8f8bcc1c428ed0e0d7a3bf699044bb63a3187860`

```dockerfile
```

-	Layers:
	-	`sha256:5ea59cb371837732653ec05ca8dda265f45219fd149838f788d277ebdbaa0c71`  
		Last Modified: Thu, 22 May 2025 04:11:45 GMT  
		Size: 7.3 MB (7267532 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa42f348f4fd61c12d93b308776689b6ee4d192f279d2c99f6e468b2ee283376`  
		Last Modified: Thu, 22 May 2025 04:11:45 GMT  
		Size: 15.8 KB (15790 bytes)  
		MIME: application/vnd.in-toto+json

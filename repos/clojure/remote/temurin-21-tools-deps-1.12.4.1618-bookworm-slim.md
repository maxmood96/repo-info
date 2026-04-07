## `clojure:temurin-21-tools-deps-1.12.4.1618-bookworm-slim`

```console
$ docker pull clojure@sha256:5ce548094169e09d58315842604d260df10ff7ba87f47a32ef9820f7e11b2b94
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

### `clojure:temurin-21-tools-deps-1.12.4.1618-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:065c564d6d2d3bd9f8e7b292cfbee803b2c8de230a764ad057d0d941ae345c9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.8 MB (255797137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abbd6e20dec967d970c1ede8a03f9bd636ad30f0f35b692be2866f6979d2c96d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 03:16:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 03:16:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 03:16:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:16:12 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 07 Apr 2026 03:16:12 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 03:16:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 07 Apr 2026 03:16:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 07 Apr 2026 03:16:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 07 Apr 2026 03:16:26 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 07 Apr 2026 03:16:26 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:da539b6761059a0a114c6671f1267b57445e3a54da023db5c28be019e40f0284`  
		Last Modified: Tue, 07 Apr 2026 00:11:03 GMT  
		Size: 28.2 MB (28236332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7cb3df506c3a9a1a8a69607be89532871fdf1bffc090f826a2c26381c376f77`  
		Last Modified: Tue, 07 Apr 2026 03:16:50 GMT  
		Size: 157.9 MB (157857091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49c255ea629786e8c1e11f7668ac67690678f1ec2f2192d6b4dcfafdb0c538fd`  
		Last Modified: Tue, 07 Apr 2026 03:16:48 GMT  
		Size: 69.7 MB (69702671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f0e7bbc33cbc0b31fb37c202c33139faff52ac45f733c88b848fef7de836b49`  
		Last Modified: Tue, 07 Apr 2026 03:16:45 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c63e87b4b8fad12538adf62032b02def80a0368dfd6480af0517608c585f01dd`  
		Last Modified: Tue, 07 Apr 2026 03:16:45 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.4.1618-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:10fe90ec60222228c918068dd55afa3d882d632b57c26d0b13d8be9802e0d1de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5133855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1b41d1a4125c2b2facdf3dff422896ec3584d783eb947d428177bf797544433`

```dockerfile
```

-	Layers:
	-	`sha256:fb7a1f9df241859f54baa1e178ae7ff0aeed0d9dc65cfd4dd59ef13d0174b101`  
		Last Modified: Tue, 07 Apr 2026 03:16:46 GMT  
		Size: 5.1 MB (5118019 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05a21b050be13795e006ede13ff9f4476df5ef16736167b73af8369f60a51cd0`  
		Last Modified: Tue, 07 Apr 2026 03:16:45 GMT  
		Size: 15.8 KB (15836 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.4.1618-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:431583aaa58a3635307cfdb7211d02ac1f0ffec8365cf0bc80161633cca4ca95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.9 MB (253939248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3616dd1bd281211c02e981943a6cc45d70cc049387b14d45b1ea89d9b5f45ca5`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 03:26:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 03:26:48 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 03:26:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:26:48 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 07 Apr 2026 03:26:48 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 03:27:03 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 07 Apr 2026 03:27:03 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 07 Apr 2026 03:27:03 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 07 Apr 2026 03:27:03 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 07 Apr 2026 03:27:03 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1dbbb2db815c2527e90ef5a3e4dfb957cfe7b61b6a7fc59722f1f64b1a1b611e`  
		Last Modified: Tue, 07 Apr 2026 00:10:39 GMT  
		Size: 28.1 MB (28116166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af26a674dae215114df74ec87bedafdea871fc1aad977d96cbfcfd1a56b9e1c0`  
		Last Modified: Tue, 07 Apr 2026 03:27:27 GMT  
		Size: 156.1 MB (156133030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4609ba51e4f17d787ca8cffa547672258ada1f4db47f784ea3db2113cabacc55`  
		Last Modified: Tue, 07 Apr 2026 03:27:25 GMT  
		Size: 69.7 MB (69689008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7e4b624e4769708679a02a070708311ef3a6f79cbe2c530d446e4138f01fc81`  
		Last Modified: Tue, 07 Apr 2026 03:27:22 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c02ec6d67e8bea273f0c1699254b544e3be1bb2c60730c6ee53cee5289716876`  
		Last Modified: Tue, 07 Apr 2026 03:27:22 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.4.1618-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:5846408df329c95f4380a4a6da418bb5a2fc906fb63203e04079a716a6a222a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5139734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cefb797bdd02ec690a2361ab7cc2d6f82458dd30cfa7ac15ec7775322976f56d`

```dockerfile
```

-	Layers:
	-	`sha256:1a6fcd9656a427f7e1ae02bb7e63eb5e796e5231cedd5dd2c25f3fd05e14e057`  
		Last Modified: Tue, 07 Apr 2026 03:27:23 GMT  
		Size: 5.1 MB (5123780 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d5773f850571e747ebc473cdb180314a375869b0910534e2c7a5c866cd8a1f3`  
		Last Modified: Tue, 07 Apr 2026 03:27:22 GMT  
		Size: 16.0 KB (15954 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.4.1618-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:30c3648fc65e4df6a2096409881aaefda523b69d123095c873951c904c00cf0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.6 MB (265590628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2dc10c70de82838d22b42298c941c37fc5af5d80dc92af97c71ba1b1527452b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 18:34:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 18:34:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 18:34:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 18:34:34 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 17 Mar 2026 18:34:34 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 18:40:12 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Mar 2026 18:40:13 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Mar 2026 18:40:14 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Mar 2026 18:40:14 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Mar 2026 18:40:14 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:7a0392d98c02d4219c67a8e3d3837c1ac5d4af6836b9264bdd6c427cc7a24f76`  
		Last Modified: Mon, 16 Mar 2026 21:51:26 GMT  
		Size: 32.1 MB (32078368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c08aa22040562fcd55bbeb76a004a8c37c790885d218b8fc4c0ba2c08d72b2f3`  
		Last Modified: Tue, 17 Mar 2026 18:36:05 GMT  
		Size: 158.0 MB (157977514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5df25cabb57ad1f950a08163ed25169c098ae555f97a67ae129c798995c4de8b`  
		Last Modified: Tue, 17 Mar 2026 18:40:56 GMT  
		Size: 75.5 MB (75533702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ca536a2d7f4e827ccc9ba9609ca6b47e0afae8d67c1e5fd6930dd3dc6a6a918`  
		Last Modified: Tue, 17 Mar 2026 18:40:50 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9a954452be50da89565671c5e7fbe8b6ccadf6901a54b9b1922c9597c730840`  
		Last Modified: Tue, 17 Mar 2026 18:40:50 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.4.1618-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:3bc89f23880ecb262aaa0eabf1f1ed26cfbc19fa40c676a6dd734a28c0291488
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5139061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8459d2952507e288f589e95057d3ada724c3d6c9913f04d01d30a330e400f117`

```dockerfile
```

-	Layers:
	-	`sha256:952f133ae9a16f84e6d057850aaa166a84252a87ac60807caab1155410735f18`  
		Last Modified: Tue, 17 Mar 2026 18:40:52 GMT  
		Size: 5.1 MB (5123177 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6e89e643f591d4b7e54fb8a52bf5bec231b8621797976bc3dbcf9e51c96f058`  
		Last Modified: Tue, 17 Mar 2026 18:40:50 GMT  
		Size: 15.9 KB (15884 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.4.1618-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:44f223a69d5f53c274ecd11b22382f071cb2d05e4fd065b83717cc703b5438b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.5 MB (242511489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ec484e5e5d9326d4632191f9f6c26720ccc00aae4b9acb9a4b90e31f3e2543d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 05:44:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 05:44:24 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 05:44:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 05:44:24 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 07 Apr 2026 05:44:24 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 05:45:38 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 07 Apr 2026 05:45:38 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 07 Apr 2026 05:45:38 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 07 Apr 2026 05:45:38 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 07 Apr 2026 05:45:38 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c23087fbbda0d8352ee6b2d159c503459acb89da0eba1729b411ca394e68e292`  
		Last Modified: Tue, 07 Apr 2026 00:10:59 GMT  
		Size: 26.9 MB (26891634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8e7319be332fb7a0de839eaf561970a3169c636f32f76719336639dcb74ddbe`  
		Last Modified: Tue, 07 Apr 2026 05:45:06 GMT  
		Size: 147.1 MB (147105212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80d106a1b954b408153331fabf9a1f0cbccdf03fc37cd0fd3b5692f19ef63ec6`  
		Last Modified: Tue, 07 Apr 2026 05:46:03 GMT  
		Size: 68.5 MB (68513598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6215f2ffa5a1612f1114087ff3cb66c2a96dca086fbc04ccf9cd072797052706`  
		Last Modified: Tue, 07 Apr 2026 05:46:00 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d14646b084e2627d487156d5b9840095ab918f4d4db4cfd74f0a37a7ae8e5e81`  
		Last Modified: Tue, 07 Apr 2026 05:46:01 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.4.1618-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:800c0cb28c5167772109d0815abc3347e249a61554ed8a70b13ca1912af23ee4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5125176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8718e3da76040047aaef7e4210019fcc6e35348516fe12fb16278c7f57a0b2fd`

```dockerfile
```

-	Layers:
	-	`sha256:1e90ded8220091849133f854333918e2f7a0ec2b40c17e5a7ab7516050274ffb`  
		Last Modified: Tue, 07 Apr 2026 05:46:01 GMT  
		Size: 5.1 MB (5109340 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c94d26a2c8064434138e47a2b9bb99a68e49cd9ef2c459916f5c813a96fc517`  
		Last Modified: Tue, 07 Apr 2026 05:46:01 GMT  
		Size: 15.8 KB (15836 bytes)  
		MIME: application/vnd.in-toto+json

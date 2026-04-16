## `clojure:temurin-21-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:04830fb759f630d4fdc0e24cb28fdd1d6c5c056e2b2643f32b919de07247b366
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
$ docker pull clojure@sha256:a298c035c6fb5bb9f1b5515c17deeb54439b82711053774fc53866c798ecdfb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.8 MB (255793540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4534c9f46fcc7588e26f184e7342ba630a8d3247c27ffcb53928334b16cdb77c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1775433600'
# Wed, 15 Apr 2026 22:05:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 22:05:40 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 22:05:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:05:40 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 15 Apr 2026 22:05:40 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:05:55 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 15 Apr 2026 22:05:55 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 15 Apr 2026 22:05:55 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 15 Apr 2026 22:05:55 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 15 Apr 2026 22:05:55 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:da539b6761059a0a114c6671f1267b57445e3a54da023db5c28be019e40f0284`  
		Last Modified: Tue, 07 Apr 2026 00:11:03 GMT  
		Size: 28.2 MB (28236332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1374c734028c648fe6f3031ef4de1c45fa331fbc1812bc39fdde14ba1bfd433`  
		Last Modified: Wed, 15 Apr 2026 22:06:19 GMT  
		Size: 157.9 MB (157857082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b8ba986d574e7adb8241a6ecb82962af5a38c19744739071ba0b191f7ef0b58`  
		Last Modified: Wed, 15 Apr 2026 22:06:17 GMT  
		Size: 69.7 MB (69699081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61e1e0c04ce8bc99eb0c9f8f56aca87ab9fcac9b0b4e54499497ced92bf76d8f`  
		Last Modified: Wed, 15 Apr 2026 22:06:13 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4a243cc90f6d2a2e0958dadd0073f0b0d40ea1a2cd02824b526d74520e4bc5b`  
		Last Modified: Wed, 15 Apr 2026 22:06:13 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:12548697b9bf74c4e217e44e1e863c82c54065ebc75039a02b4ee6061ebf54fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5133855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b60b6668b832c3d617d8426ef8099d919b3c6e7be7a8f42c5e3b60c341e15c5`

```dockerfile
```

-	Layers:
	-	`sha256:10ab5020e9c0c1b44c6998b8a57e458af7847b2e6ce9545a9906abdbd8e12cc8`  
		Last Modified: Wed, 15 Apr 2026 22:06:14 GMT  
		Size: 5.1 MB (5118019 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:820201f13460df0a189d3a7ff1bb684cd4d5e132c46548b9c4c07848dbecbb2f`  
		Last Modified: Wed, 15 Apr 2026 22:06:13 GMT  
		Size: 15.8 KB (15836 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-bookworm-slim` - linux; arm64 variant v8

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

### `clojure:temurin-21-tools-deps-bookworm-slim` - unknown; unknown

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

### `clojure:temurin-21-tools-deps-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:01ce26d63c5fbc2e009e1792afb7e01e5a0e45c00b1d7dc3130baff07e51ae16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.6 MB (265590702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb14d1886c3f1c597e1f153fc3dcd28640882d20f6e340230928552ee00cff55`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 14:45:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 14:45:56 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 14:45:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 14:45:56 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 07 Apr 2026 14:45:56 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 14:50:29 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 07 Apr 2026 14:50:30 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 07 Apr 2026 14:50:30 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 07 Apr 2026 14:50:30 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 07 Apr 2026 14:50:30 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b1c56220ca211bc9d02f1ed5c589465809676b6ab2cef705f1e2fb8e9726de76`  
		Last Modified: Tue, 07 Apr 2026 00:09:42 GMT  
		Size: 32.1 MB (32078464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3e0e1fa8857b496e254e0f7876a400c7f64ae5a188234bb52567d6106153125`  
		Last Modified: Tue, 07 Apr 2026 14:47:20 GMT  
		Size: 158.0 MB (157977538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa3b41b69a1d9bb843e2c9f3f579bfb2eb70bff5a7f3040dd72d5a7cd6c16d7c`  
		Last Modified: Tue, 07 Apr 2026 14:51:05 GMT  
		Size: 75.5 MB (75533656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e377b6471e303d48bafd22eaef0ac32dfdc6a3da6b3477a0c06a11d845c9f3a`  
		Last Modified: Tue, 07 Apr 2026 14:51:03 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:505aa6e52f308fb295b01e102ca9a7cee8bd058604a50ef0a3a2c6834d290838`  
		Last Modified: Tue, 07 Apr 2026 14:51:03 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:905432b0edc3d7f8aeeec86dcb994f5efda6c13065f72dc2a9c7046e2f366f8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5139060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3c40130540324256c16b65c6b62e2cec27bdb45ae51381036111e37da18c6ec`

```dockerfile
```

-	Layers:
	-	`sha256:1340f139c76c04970cfcc20a4ca80cbd64de4c8026ccea858d820ecd28dffacc`  
		Last Modified: Tue, 07 Apr 2026 14:51:03 GMT  
		Size: 5.1 MB (5123177 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b6cdb7afcdfa582b163088d8f8b27c71912969fa134e8411c398974844db3cd`  
		Last Modified: Tue, 07 Apr 2026 14:51:03 GMT  
		Size: 15.9 KB (15883 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-bookworm-slim` - linux; s390x

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

### `clojure:temurin-21-tools-deps-bookworm-slim` - unknown; unknown

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

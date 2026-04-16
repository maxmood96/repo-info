## `clojure:temurin-21-tools-deps`

```console
$ docker pull clojure@sha256:3f0664e987e9c32a4be21aa494cc4a06126708e6f6e4ddc975781bde4a4e9410
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

### `clojure:temurin-21-tools-deps` - linux; amd64

```console
$ docker pull clojure@sha256:bb1332b148570acd8e026a181708bc65f1311e6c8161ec19466d7560ba6f7dfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.5 MB (287513352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:114934c787e3f3dee8cf32a2d0fa18f79eb3319b25043f1122a4c810f9000e55`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1775433600'
# Wed, 15 Apr 2026 22:05:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 22:05:16 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 22:05:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:05:16 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 15 Apr 2026 22:05:16 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:05:31 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 15 Apr 2026 22:05:31 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 15 Apr 2026 22:05:31 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 15 Apr 2026 22:05:31 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 15 Apr 2026 22:05:31 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c150dd3f5fc91eabd1818cc30298a4a956782621583cadfd369c4d327584008e`  
		Last Modified: Tue, 07 Apr 2026 00:10:26 GMT  
		Size: 48.5 MB (48488823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdfc807d263e14d09a0c0c239598fdf5fdb38c7beb75974194be9dacaa976b09`  
		Last Modified: Wed, 15 Apr 2026 22:05:56 GMT  
		Size: 157.9 MB (157857054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7e8c816ad3da8590935f328e0a4c8055e14283e20957b65a3c52dcc42bacff1`  
		Last Modified: Wed, 15 Apr 2026 22:05:54 GMT  
		Size: 81.2 MB (81166433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dc1894a37a64257ff9adb53753d7db4b706565d3c88d4849008952f0d14ecf6`  
		Last Modified: Wed, 15 Apr 2026 22:05:51 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f476cb4c51c91acbf6a464fc4c5e4de62978c4fb83c60bf6580f32155da8a11`  
		Last Modified: Wed, 15 Apr 2026 22:05:50 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps` - unknown; unknown

```console
$ docker pull clojure@sha256:84357aeed88f65f52e23397ca2d42eecbbdd451b8fd2367a800ea734be745b08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7397300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48786e0b28c055c51222cacb7016dcbac6d5c72e1991f80d57b3b8990656c853`

```dockerfile
```

-	Layers:
	-	`sha256:31c4b49a0941f4aa78d62e8dba0a4c49ca90ba162a18c5d483fafa10102d2e45`  
		Last Modified: Wed, 15 Apr 2026 22:05:51 GMT  
		Size: 7.4 MB (7380838 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:362e0268296369cd4dd2e21a05613cd8920e946301e3e2df29ac6518d8724c13`  
		Last Modified: Wed, 15 Apr 2026 22:05:50 GMT  
		Size: 16.5 KB (16462 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:0de4469aa4dfa8df2fbd54c583202d0eb5a2db1f52b5a0155ec84fa7ac961322
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.7 MB (285665638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66ced0f5fa1e1cac1ea4f1c8fdf4ed581dc6f915970b5dba859ac0327eb5be90`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 03:26:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 03:26:58 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 03:26:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:26:58 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 07 Apr 2026 03:26:58 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 03:27:15 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 07 Apr 2026 03:27:15 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 07 Apr 2026 03:27:15 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 07 Apr 2026 03:27:15 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 07 Apr 2026 03:27:15 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:d03e31a3f7ef0d2866d799846c3a18286fab6fcddbd8c523f3cb5ed1bd2f31a3`  
		Last Modified: Tue, 07 Apr 2026 00:10:26 GMT  
		Size: 48.4 MB (48373262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:249f97a7810f7c4fb76a40f9834ad59904c453f7b015588f06f9cdb000d15563`  
		Last Modified: Tue, 07 Apr 2026 03:27:41 GMT  
		Size: 156.1 MB (156133048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc434ffe318a084c587d54adc25f1b3da1e664c9e9795994d4a3b53db45fb5df`  
		Last Modified: Tue, 07 Apr 2026 03:27:39 GMT  
		Size: 81.2 MB (81158285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3072b97b5dff8a72c0354b5c33eaf8ed06019f8c1960459132949519b4480daa`  
		Last Modified: Tue, 07 Apr 2026 03:27:36 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd8c7f8c89d0d3fe2c294e8858fb6ae0cb5ab846ffa026ab5037f88998b16225`  
		Last Modified: Tue, 07 Apr 2026 03:27:36 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps` - unknown; unknown

```console
$ docker pull clojure@sha256:a139e81e64c441a46342ad8d87c31922575d99fbe54e7f3a1151feee432ce7cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7403229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:218274f2df53422fdec2ecef906a8c6e76ebafb9f62f7c9d2a388dbd26232da7`

```dockerfile
```

-	Layers:
	-	`sha256:87175d95d93a825ab235de5da4605841b29ee3ea2a22131ffd468f3cdc420114`  
		Last Modified: Tue, 07 Apr 2026 03:27:36 GMT  
		Size: 7.4 MB (7386625 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23449a86138e7f2a4227a2ec0d3fa203f03676cc76a33ee1f0ed4de8aa7aab6c`  
		Last Modified: Tue, 07 Apr 2026 03:27:35 GMT  
		Size: 16.6 KB (16604 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps` - linux; ppc64le

```console
$ docker pull clojure@sha256:df2243cd0929a4d0788d30640b38f729afbe193c3326db520399b8ddbbab8527
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.3 MB (297315852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc7bc36c630f65a24e0c442270fd02bc814be83a2833e4d835a903900acc6f00`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 14:45:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 14:45:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 14:45:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 14:45:11 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 07 Apr 2026 14:45:11 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 14:50:19 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 07 Apr 2026 14:50:21 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 07 Apr 2026 14:50:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 07 Apr 2026 14:50:26 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 07 Apr 2026 14:50:26 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6b775f7ad22043f8bb75d535d8a1279e43453a08a4a9e6a0b48c020c9b387079`  
		Last Modified: Tue, 07 Apr 2026 00:09:43 GMT  
		Size: 52.3 MB (52336938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46e3fef080cc35cf9b72cdc460d1508c5e1620da32f827f1d747773b4bb79804`  
		Last Modified: Tue, 07 Apr 2026 14:46:39 GMT  
		Size: 158.0 MB (157977496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abcb89939229a33552c251cd4f1ee5e8160da63471e61c861fc5329bd2d5caf5`  
		Last Modified: Tue, 07 Apr 2026 14:51:08 GMT  
		Size: 87.0 MB (87000375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43400e60b3380d7076185d0743571e9f2c3eade8dbcd0dad4b0cb754fd8cc6cc`  
		Last Modified: Tue, 07 Apr 2026 14:51:06 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3606f692a55b5e6a2dee7efec1a48395c0465a3eaf122cc158be168dcbb2ba73`  
		Last Modified: Tue, 07 Apr 2026 14:51:06 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps` - unknown; unknown

```console
$ docker pull clojure@sha256:e1fe23d8930b88828521931b9e197f5041c243f9ff57ac8972da2d94e7e53658
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7402588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b881aeef07acc23829cf3cc1356a6a2797d41932f9e6740eb40e1075ee105213`

```dockerfile
```

-	Layers:
	-	`sha256:3a5333b1b9c99e259c8d48966ec538b19f1c720287487cf35d80623dbbb8156a`  
		Last Modified: Tue, 07 Apr 2026 14:51:06 GMT  
		Size: 7.4 MB (7386066 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2834207053ace4f5aeb310fecf132b5a9d012635133e111a1c8c0e8ab23dec8d`  
		Last Modified: Tue, 07 Apr 2026 14:51:06 GMT  
		Size: 16.5 KB (16522 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps` - linux; s390x

```console
$ docker pull clojure@sha256:59c4590c29425589251ee56d2a282b48f4ab630d99656b77eb8ba1420c078f33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.2 MB (274242416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8fbc4484c0bae0164309a29b577135aac1b9b98cb08fe6622a848d7186f9b07`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 05:45:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 05:45:16 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 05:45:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 05:45:16 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 07 Apr 2026 05:45:16 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 05:45:30 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 07 Apr 2026 05:45:30 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 07 Apr 2026 05:45:30 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 07 Apr 2026 05:45:30 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 07 Apr 2026 05:45:30 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:40ecbf1d4e17f6b072e6cef463823baec601d9f21c9dc33d98bd258448a986f6`  
		Last Modified: Tue, 07 Apr 2026 00:10:32 GMT  
		Size: 47.1 MB (47148084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa37d5d2197c3cb308ae61c0aee840666757f96b738357351f34685c9b11dae0`  
		Last Modified: Tue, 07 Apr 2026 05:46:02 GMT  
		Size: 147.1 MB (147105213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fab8f70c91ea80705dcf858669d0f675b0b9e7da6dd566071761ea8225cbf07c`  
		Last Modified: Tue, 07 Apr 2026 05:46:01 GMT  
		Size: 80.0 MB (79988077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eb331fcefbe6696e48c23962bee8fd99353f65bd608183e1c44aac8a24fe3c9`  
		Last Modified: Tue, 07 Apr 2026 05:45:58 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8350dc513b6067d393b39b3859d221f1095542fa2b18fa20f89caf269df2e8c`  
		Last Modified: Tue, 07 Apr 2026 05:45:58 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps` - unknown; unknown

```console
$ docker pull clojure@sha256:c9036463172a974ab2d3de77769a0805fd4320e11926f34676c1b76723621622
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7388619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3195ee98f50f328022f48cd5b304de4192ac3ae090dc546145d1f4a2d12a4391`

```dockerfile
```

-	Layers:
	-	`sha256:f797e0982dcee58776d6355266d5128b5e99ddad2ddec7e426c53e151433a86f`  
		Last Modified: Tue, 07 Apr 2026 05:45:59 GMT  
		Size: 7.4 MB (7372157 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8d6c4f8c78254988abcabc2e8fc3f8d9e53fdb55bccea4d3bc5f5824b755c7d`  
		Last Modified: Tue, 07 Apr 2026 05:45:58 GMT  
		Size: 16.5 KB (16462 bytes)  
		MIME: application/vnd.in-toto+json

## `clojure:temurin-25-tools-deps`

```console
$ docker pull clojure@sha256:cb073b6febebc133a5ace6f9afb40f382774181cf5c413fdc13c4b1434cd1ab5
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

### `clojure:temurin-25-tools-deps` - linux; amd64

```console
$ docker pull clojure@sha256:24b7b14d162eeee18c89f58b6d1a754e2d2811d712ac599f3ff3cc228b592dc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.9 MB (221923473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a228bff6d00c2390c2d5fbc587fb93f7bee3c50b353fcab9a80ab9e06f1f0011`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Wed, 04 Mar 2026 17:51:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 04 Mar 2026 17:51:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 04 Mar 2026 17:51:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Mar 2026 17:51:21 GMT
ENV CLOJURE_VERSION=1.12.4.1612
# Wed, 04 Mar 2026 17:51:21 GMT
WORKDIR /tmp
# Wed, 04 Mar 2026 17:51:35 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "21d16fbce3e546c4f0163c78aba0eb0293993c7fa1aba77d089fdbfa445e38a2 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 04 Mar 2026 17:51:35 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 04 Mar 2026 17:51:35 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 04 Mar 2026 17:51:35 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 04 Mar 2026 17:51:35 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6a7e0620566c7dfbe5d3c9a7601d116556ec17a021b3e824f8ab09d12b0c25c6`  
		Last Modified: Tue, 24 Feb 2026 18:42:43 GMT  
		Size: 48.5 MB (48488777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff260d5b9822a119863769c1050ac9895f3e596956fdae3893bbc3dd37bde2ee`  
		Last Modified: Wed, 04 Mar 2026 17:51:57 GMT  
		Size: 92.3 MB (92256302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c72d677291271a51a098e24dd9af2f720a029b7c4f7583e9024e5f0f623097f2`  
		Last Modified: Wed, 04 Mar 2026 17:51:57 GMT  
		Size: 81.2 MB (81177352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22115ec4e2dc20610c653b40019c10f948ee756052b2f0ceb65803d519716956`  
		Last Modified: Wed, 04 Mar 2026 17:51:54 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fdf3c067330f133019f34524f6dc7f67c88a9bce469dc8f0514ea94743799b3`  
		Last Modified: Wed, 04 Mar 2026 17:51:54 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps` - unknown; unknown

```console
$ docker pull clojure@sha256:3742272e79ebcdd23042fa6aaef78ac7c614fd7f9fd7f07118f148d836ecd84a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7365470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64f84ad4209fbdc07d7e0cd8d5b9eb0c9fc902216ba5f3263f07287d1abccb37`

```dockerfile
```

-	Layers:
	-	`sha256:dd1798c8fa3cf2a6f4253b15c25b1d5389ded73ae9a63eb2ba4a49da6a9d0575`  
		Last Modified: Wed, 04 Mar 2026 17:51:54 GMT  
		Size: 7.3 MB (7347700 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7190f9d7f1bb66717b3084ceab5903a82cf51d7ec9389478482538fb87de7f31`  
		Last Modified: Wed, 04 Mar 2026 17:51:54 GMT  
		Size: 17.8 KB (17770 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:2423e1be165ddf678da2160da2ad15a67101b8b7026d505fb1d527b2d8cd041f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.8 MB (220820642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db39d482f8e5cfc1aa3584c7860ddd49fa42735e4ee54f0effe28e78b299090a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1771804800'
# Wed, 04 Mar 2026 17:50:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 04 Mar 2026 17:50:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 04 Mar 2026 17:50:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Mar 2026 17:50:46 GMT
ENV CLOJURE_VERSION=1.12.4.1612
# Wed, 04 Mar 2026 17:50:46 GMT
WORKDIR /tmp
# Wed, 04 Mar 2026 17:51:02 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "21d16fbce3e546c4f0163c78aba0eb0293993c7fa1aba77d089fdbfa445e38a2 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 04 Mar 2026 17:51:02 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 04 Mar 2026 17:51:02 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 04 Mar 2026 17:51:02 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 04 Mar 2026 17:51:02 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:8578011282ae3fef36307f7e3afb2265a96bada1a57648f07bea9cc1a11e7b7b`  
		Last Modified: Tue, 24 Feb 2026 18:42:06 GMT  
		Size: 48.4 MB (48373210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0af92ad2013fc7a909aee75f0afe6f4af5f2cb085b95d58a730ff48167ed65e`  
		Last Modified: Wed, 04 Mar 2026 17:51:24 GMT  
		Size: 91.3 MB (91288274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c758d01704dc49edc77b39ac1edfa014879d61dd1ccfb4c4384661ad0249b83c`  
		Last Modified: Wed, 04 Mar 2026 17:51:24 GMT  
		Size: 81.2 MB (81158115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11984492652e5cba97418d5486fe78d76cbbbafd34fe5f77b179e6700811b701`  
		Last Modified: Wed, 04 Mar 2026 17:51:21 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32c00788dd35a8b5e0b0dddb6c423cdc023cf73feaadff51018f48df7e68bea3`  
		Last Modified: Wed, 04 Mar 2026 17:51:21 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps` - unknown; unknown

```console
$ docker pull clojure@sha256:4db43bed8ac381f39ec450482eb1ee92a942daea47622bcb1eb8aa92713cc642
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7371493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d04c7a237d0dc6b98faaced3b1bde46dedea3583e774cb25e6370804ab5cedac`

```dockerfile
```

-	Layers:
	-	`sha256:7b38c7fda2b67e4d395051620cab87b5dc1ac3bd5db2e70527a7814e3625c0be`  
		Last Modified: Wed, 04 Mar 2026 17:51:21 GMT  
		Size: 7.4 MB (7353532 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90804d0aa09a68d79f48542ed50756b60b2d61ee42d8a5f1414930341e21c7e2`  
		Last Modified: Wed, 04 Mar 2026 17:51:21 GMT  
		Size: 18.0 KB (17961 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps` - linux; ppc64le

```console
$ docker pull clojure@sha256:2acab766f31e8d087f62fc9a04795161e46688acba3ac306b7978b8bcd2ce900
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.0 MB (230970494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d24810d1d45f93435f4d9d934ffffa5cefca4a55e80edb5e2e6b9768bc4f273`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1771804800'
# Mon, 02 Mar 2026 19:43:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 02 Mar 2026 19:43:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 02 Mar 2026 19:43:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Mar 2026 19:43:33 GMT
ENV CLOJURE_VERSION=1.12.4.1612
# Mon, 02 Mar 2026 19:43:34 GMT
WORKDIR /tmp
# Wed, 04 Mar 2026 18:09:30 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "21d16fbce3e546c4f0163c78aba0eb0293993c7fa1aba77d089fdbfa445e38a2 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 04 Mar 2026 18:09:31 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 04 Mar 2026 18:09:31 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 04 Mar 2026 18:09:31 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 04 Mar 2026 18:09:31 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:605d3e8e339092bb5c341e87f55fee22f143aaa738eb91d341b5fc6aa27b2b5b`  
		Last Modified: Tue, 24 Feb 2026 18:41:51 GMT  
		Size: 52.3 MB (52336797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:144f17a3e7d82510fe9dc0d0bcec634fee1e230b910b421966d0efc2cada5dc0`  
		Last Modified: Mon, 02 Mar 2026 19:46:31 GMT  
		Size: 91.6 MB (91632868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f56ad74f553334ce0b4b46b803421e82329835fc60c83465b6a07bb726594b1`  
		Last Modified: Wed, 04 Mar 2026 18:10:08 GMT  
		Size: 87.0 MB (86999783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09e6f6215da1505344c447d2642724b57473f9e37ba0a75e0061d8e1a99ed753`  
		Last Modified: Wed, 04 Mar 2026 18:10:06 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fe11ba96c4121745bb70ef0acee845877ad000649e382c09c8c1939a56779b2`  
		Last Modified: Wed, 04 Mar 2026 18:10:06 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps` - unknown; unknown

```console
$ docker pull clojure@sha256:0afb0f3c7cd9c1a8c194d96f6bda64814b3dfc8b967924340ba8921d9d27b21d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7353320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b1c102d4b9a3693e648ba47fd4fc8a325b8c7233dd36e422211ce10eaf843ad`

```dockerfile
```

-	Layers:
	-	`sha256:52f140053ca6df1c4fe3bc033fa49217bd3bc4680e485ef2a9028d9f576a066d`  
		Last Modified: Wed, 04 Mar 2026 18:10:06 GMT  
		Size: 7.3 MB (7336264 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43adc06e90104fc31827a90be229ff935be8d6415f0187cd2fa69d197101caa5`  
		Last Modified: Wed, 04 Mar 2026 18:10:06 GMT  
		Size: 17.1 KB (17056 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps` - linux; s390x

```console
$ docker pull clojure@sha256:ee23e9a8b72a7e7500bd2f05c3806033a5cd87eaca6280acd55b402665e2ada3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.4 MB (215371139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25104cbed305d53532b471130c6af8d78c5200f72edc482a079f4e80fd2e7090`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1771804800'
# Wed, 04 Mar 2026 17:51:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 04 Mar 2026 17:51:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 04 Mar 2026 17:51:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Mar 2026 17:51:29 GMT
ENV CLOJURE_VERSION=1.12.4.1612
# Wed, 04 Mar 2026 17:51:29 GMT
WORKDIR /tmp
# Wed, 04 Mar 2026 17:51:43 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "21d16fbce3e546c4f0163c78aba0eb0293993c7fa1aba77d089fdbfa445e38a2 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 04 Mar 2026 17:51:43 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 04 Mar 2026 17:51:43 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 04 Mar 2026 17:51:43 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 04 Mar 2026 17:51:43 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:00b1871f38dea81b1982e306480bd9f97cedf7b0cb3342e4bc84925e6082ade8`  
		Last Modified: Tue, 24 Feb 2026 18:41:26 GMT  
		Size: 47.1 MB (47148087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac9e91a589f700a01da108355aea6ed7db00154ea17ea5fe5c67507fd6e1feb1`  
		Last Modified: Wed, 04 Mar 2026 17:52:13 GMT  
		Size: 88.2 MB (88233824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22d9451129fc31c7e3eafc179a312fcb25a5475c62215ba76aadee48eb95d5ef`  
		Last Modified: Wed, 04 Mar 2026 17:52:13 GMT  
		Size: 80.0 MB (79988186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16068c443f9492ade34656d89fbad94df1458800c1e60dca40b5e4bdd9bdfcbd`  
		Last Modified: Wed, 04 Mar 2026 17:52:11 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6d7f4f17cd75119650f7b21ec5178c16297eddabf909f239d837162160c469e`  
		Last Modified: Wed, 04 Mar 2026 17:52:10 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps` - unknown; unknown

```console
$ docker pull clojure@sha256:98b3f21f3d589070e765ac79c6d7f094bafe44acb3c501105a4ac1f7af5b89ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7341352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bac465cb48e64f81dfa94884fa710d3adf9b1d63a5de95d6f5ebe0ee8356e17a`

```dockerfile
```

-	Layers:
	-	`sha256:6a408bc8161b9ca094f4514a108ba9520710e06859b8354b35f9cf94b8d72dee`  
		Last Modified: Wed, 04 Mar 2026 17:52:11 GMT  
		Size: 7.3 MB (7323581 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56028bfc3380d633d59cce614662f1246b5155a4a5424ae79da735cf06f5ce69`  
		Last Modified: Wed, 04 Mar 2026 17:52:10 GMT  
		Size: 17.8 KB (17771 bytes)  
		MIME: application/vnd.in-toto+json

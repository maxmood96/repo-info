## `clojure:temurin-21-tools-deps-trixie`

```console
$ docker pull clojure@sha256:08febfa48ec523f32ee5f7c0c4571acb6aade833073409b8552688e0188c6d1d
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

### `clojure:temurin-21-tools-deps-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:73fa4b8536ca773a0293742009f27b86137e316cdfcb00f90d5c0270d486bfcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.1 MB (293074312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3954123afb1381426d23fdaade4c4974b5b7c3e516f537a60096516499310b24`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Thu, 14 May 2026 23:35:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 May 2026 23:35:57 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 14 May 2026 23:35:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 May 2026 23:35:57 GMT
ENV CLOJURE_VERSION=1.12.5.1638
# Thu, 14 May 2026 23:35:57 GMT
WORKDIR /tmp
# Thu, 14 May 2026 23:36:15 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bccfca8c437514786f0827a11195b89b833357b2a668091f4321b451b2e36df5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 14 May 2026 23:36:15 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 14 May 2026 23:36:15 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 14 May 2026 23:36:15 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 14 May 2026 23:36:15 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:307f8152a55ef1e9eeb1acbbee7bc81232615329eaeb00d8dd93b46be297f34c`  
		Last Modified: Fri, 08 May 2026 18:24:07 GMT  
		Size: 49.3 MB (49302320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7d54befd331fd0937d266b32b504271eff2564525849a61a064b9aa604587a4`  
		Last Modified: Thu, 14 May 2026 23:36:36 GMT  
		Size: 158.2 MB (158166937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce9e32e2730486be61f17a4db24bb5f24565f7b76d24efbfa1d435594fdbdfbe`  
		Last Modified: Thu, 14 May 2026 23:36:40 GMT  
		Size: 85.6 MB (85604012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1ac692963e34d9dd4140c26492f2b8b58f62c14249a02e1ceb4c761425f431a`  
		Last Modified: Thu, 14 May 2026 23:36:36 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3094086cea87d21d6f2856eaf344afe69360265fefeb8c35920cf67a5252e576`  
		Last Modified: Thu, 14 May 2026 23:36:36 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:6ae176d32fda7f65c7727b87bed1fc2aa1b2de4cf20db2fddc5a61ac10d35e19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7489142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b8c634234df2d7138b38a12f07b3c6041f3a2cc71ef7f9a6f6069d4df66a01c`

```dockerfile
```

-	Layers:
	-	`sha256:1d00547ce1271f73870ae3ea7541d7d008becc85c82547dccd9fcc822cbcb99f`  
		Last Modified: Thu, 14 May 2026 23:36:36 GMT  
		Size: 7.5 MB (7473234 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36d041d84348c99b3593fd35291ff4ab3bd53bfbed77c7fc4f229d0a60f9da16`  
		Last Modified: Thu, 14 May 2026 23:36:36 GMT  
		Size: 15.9 KB (15908 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:9d0e7ca7d8f3e27b8df6622a05c288b1f122218e864582dabcaa434d604563ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.5 MB (291546860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39584545c34f2006c101b26dbe4770465d19176e8f532251812e69b7ce6f3549`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Thu, 14 May 2026 23:35:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 May 2026 23:35:59 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 14 May 2026 23:35:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 May 2026 23:35:59 GMT
ENV CLOJURE_VERSION=1.12.5.1638
# Thu, 14 May 2026 23:35:59 GMT
WORKDIR /tmp
# Thu, 14 May 2026 23:36:17 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bccfca8c437514786f0827a11195b89b833357b2a668091f4321b451b2e36df5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 14 May 2026 23:36:17 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 14 May 2026 23:36:17 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 14 May 2026 23:36:17 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 14 May 2026 23:36:17 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b5d74b688654dda99557234223479d1600781c2797759908abb12a2e782ab1ad`  
		Last Modified: Fri, 08 May 2026 18:26:51 GMT  
		Size: 49.7 MB (49669445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b5b5f2058816338917e79661cb32b706a4c265a55ccd92c8ea52bbb3c6c6558`  
		Last Modified: Thu, 14 May 2026 23:36:42 GMT  
		Size: 156.5 MB (156461329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb9fc5c1d4445f542666914ed35161b53e7181fc95a8a6b453f5c82a14806975`  
		Last Modified: Thu, 14 May 2026 23:36:41 GMT  
		Size: 85.4 MB (85415040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52fc8e8f20e929c8516056dc63f9515363ecb6b56b49dc6a79a8a708253333ae`  
		Last Modified: Thu, 14 May 2026 23:36:37 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3a67379bb8a906c93089151decaeb6a72dec88ee3d71be23780e8208b3650b4`  
		Last Modified: Thu, 14 May 2026 23:36:37 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:4ae16d380a9314a8b105f21b2293a1b7f57d75b378299da6d2520b29969a9878
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7496290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef136accb0d45db5862e91f720a3b7b32c38127de21f302ac313071248bd096a`

```dockerfile
```

-	Layers:
	-	`sha256:a7fc53641a3cf7e454fc277b122cff3eaa50579c7bb072cd5204c97b77765625`  
		Last Modified: Thu, 14 May 2026 23:36:38 GMT  
		Size: 7.5 MB (7480264 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65bc7abdce33ebfdc4651ab16f2952c33d2eb2e60f3628123194ef9574ca7a50`  
		Last Modified: Thu, 14 May 2026 23:36:37 GMT  
		Size: 16.0 KB (16026 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:0e211199e7a083800a4b1d99f1f4313b490a3ef2c1a0dd43d5b57e38e8b10e71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.5 MB (302475834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e402616b9d2411b818b6b66d321fe6a6c35daa4bb5b574558e6154423442b54b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1777939200'
# Sat, 09 May 2026 02:37:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 09 May 2026 02:37:56 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 09 May 2026 02:37:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 09 May 2026 02:37:56 GMT
ENV CLOJURE_VERSION=1.12.5.1638
# Sat, 09 May 2026 02:37:56 GMT
WORKDIR /tmp
# Thu, 14 May 2026 23:50:08 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bccfca8c437514786f0827a11195b89b833357b2a668091f4321b451b2e36df5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 14 May 2026 23:50:08 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 14 May 2026 23:50:09 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 14 May 2026 23:50:09 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 14 May 2026 23:50:09 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:95ea8643a6311b39c5ca6b858ab22e7e7fb5819831b6070e3d6390a0ebf1be97`  
		Last Modified: Fri, 08 May 2026 19:46:54 GMT  
		Size: 53.1 MB (53123165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9429fc219825eaf2a233c26bd84cdc3eef77eb70dd8fad888800a28c7609e2e4`  
		Last Modified: Sat, 09 May 2026 02:39:07 GMT  
		Size: 158.3 MB (158343282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7284e914987761976d66fe5927f4d76a9d901b8bea931fd8c922ce0f8a6493e`  
		Last Modified: Thu, 14 May 2026 23:50:50 GMT  
		Size: 91.0 MB (91008343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb2ecb5e9e12e52acbd67c46b6e31d292e8151785a98df8cf02d2dbba769cc77`  
		Last Modified: Thu, 14 May 2026 23:50:48 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da3212e16b82ba9a4841b020a3e53c55031acab445a52fd53e35375b69078018`  
		Last Modified: Thu, 14 May 2026 23:50:48 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:27f02226a5d80edd46abdeea2ed07977c91c4989f58a28035708bbb076a9d763
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7492656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f92b00e057096775efa80975e385fbed2361dc09793db473e458ed69be245d56`

```dockerfile
```

-	Layers:
	-	`sha256:045160be00fef7f90d6b614ffc1a4b86985319cedf71f8e01e745ba95b760e65`  
		Last Modified: Thu, 14 May 2026 23:50:48 GMT  
		Size: 7.5 MB (7477655 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9a88119f57575fef7d4fe74ce3a1f4e696b4aa6fa8555fef4504ce3b398504d`  
		Last Modified: Thu, 14 May 2026 23:50:47 GMT  
		Size: 15.0 KB (15001 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:e8ac884d6345965efd524d938500f463e1da41c2ec32825ad1db7b0d7769084b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.3 MB (283327438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:983e649cb3788850cad2996f85e127d00dd3e82f75dfbb0b54ac525fd393afa0`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1777939200'
# Thu, 14 May 2026 23:36:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 May 2026 23:36:41 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 14 May 2026 23:36:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 May 2026 23:36:41 GMT
ENV CLOJURE_VERSION=1.12.5.1638
# Thu, 14 May 2026 23:36:41 GMT
WORKDIR /tmp
# Thu, 14 May 2026 23:36:57 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bccfca8c437514786f0827a11195b89b833357b2a668091f4321b451b2e36df5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 14 May 2026 23:36:57 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 14 May 2026 23:36:57 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 14 May 2026 23:36:57 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 14 May 2026 23:36:57 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:49f5adf9d898afa33e019e0f5f9be5e639ceaf0c068ac396b0e56deed0761246`  
		Last Modified: Fri, 08 May 2026 18:29:56 GMT  
		Size: 49.4 MB (49372304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e440e766b22975b63d549face87d90691807326090d03ea9a9c1ba08c0abc29`  
		Last Modified: Thu, 14 May 2026 23:37:38 GMT  
		Size: 147.4 MB (147388349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10d07109d53d9a0f4a0020d2b20987cf7cef61f9d4f79215e957cf9418162b8c`  
		Last Modified: Thu, 14 May 2026 23:37:30 GMT  
		Size: 86.6 MB (86565748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e42f32a7115ae1416fce30e1e00ae9a110e703271b6ee358242f8a843554496`  
		Last Modified: Thu, 14 May 2026 23:37:24 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b860fe0b0526ec0c0f6865bc6a421fa0089da10ab6dbf37a5fe1a3e3438257cb`  
		Last Modified: Thu, 14 May 2026 23:37:24 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:7cada00096534dcfd703e2b1f22592cadd8c7ba15f04a7bbb7c3c648ffe54996
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7485062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdabaa354da39c38dd580455a2914f8645df732dcf0d7705f2c0a1fc77bdf94b`

```dockerfile
```

-	Layers:
	-	`sha256:a279f8b37abae5f66d38c7b3baf6925dd672a414a368a8b80b0d9316b05679f3`  
		Last Modified: Thu, 14 May 2026 23:37:24 GMT  
		Size: 7.5 MB (7469156 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7241575aefe8fe1ceaad3e72aa61112ee5fb976e5c5cf1cc0c12dc20ef2dac61`  
		Last Modified: Thu, 14 May 2026 23:37:24 GMT  
		Size: 15.9 KB (15906 bytes)  
		MIME: application/vnd.in-toto+json

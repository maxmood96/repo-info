## `clojure:temurin-24-tools-deps-1.12.1.1550-bookworm-slim`

```console
$ docker pull clojure@sha256:19558676edfc886939ff2bd007874ddaadf7c76519254a6dd8edb61004adbbb5
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

### `clojure:temurin-24-tools-deps-1.12.1.1550-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:1ad4955c7674b3533f31444491caeb755747cd491c451bfd8dca6b55e6d50ff1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.7 MB (187716832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c80c7bbd11acd0ba5ec56bce3920069ac5b32b5786d7bbb2d484b26103ebe1f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3da95a905ed546f99c4564407923a681757d89651a388ec3f1f5e9bf5ed0b39d`  
		Last Modified: Tue, 01 Jul 2025 01:14:43 GMT  
		Size: 28.2 MB (28230143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d08b6c90679f0c47bae60c2b1bb5af7621a7094f4b06b34679e542299b2a7a90`  
		Last Modified: Tue, 01 Jul 2025 02:40:44 GMT  
		Size: 90.0 MB (89951991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:287a209e036893c65c88fd5f2c9437f1165f03fcf919dbcb88748b1a5c2d50a4`  
		Last Modified: Tue, 01 Jul 2025 02:40:45 GMT  
		Size: 69.5 MB (69533659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84a5aaf96a9e9e0f5b97805a250704ebdda7a1d31775bd6246cdc7e2d4067df6`  
		Last Modified: Tue, 01 Jul 2025 02:40:42 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:176b42d5a00fc85a0ea676bd5b65197b3e5d0081187a9b8090959f9fff3de460`  
		Last Modified: Tue, 01 Jul 2025 02:40:42 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-1.12.1.1550-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1994fc285860cf2505e7b5454868652341c55b3807fa749414c5738b9c7dded7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5077762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5475243b7fddbd35b22ec4cac97cbe5b6b334a4a066dfdb74fa17cdb590aa565`

```dockerfile
```

-	Layers:
	-	`sha256:fc5bfb0134a81fb5f31a1d85f808f7df61a026fb5c7829a52a11611bc7a566a4`  
		Last Modified: Tue, 01 Jul 2025 06:40:19 GMT  
		Size: 5.1 MB (5061890 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6457ea6237d05b7551a9f605d02848230f11caacedc9ffb0bf649bd3852de5cd`  
		Last Modified: Tue, 01 Jul 2025 06:40:20 GMT  
		Size: 15.9 KB (15872 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-1.12.1.1550-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:ff01462a5bf09a6c6b15e8ce57df33dbb0ea5e4707e27ed7ea64b70ace146f16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.6 MB (186561176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8dc96ddf4367fcb1e57a5ef184ffd06cf329575e350ba9d2df83743d71c7e4b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1749513600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:34ef2a75627f6089e01995bfd3b3786509bbdc7cfb4dbc804b642e195340dbc9`  
		Last Modified: Tue, 10 Jun 2025 22:48:42 GMT  
		Size: 28.1 MB (28077675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7966badc2ff53635e9565b8098840d70a89a2d7fae9a20c7c38a66c6417bb6ad`  
		Last Modified: Wed, 11 Jun 2025 08:43:40 GMT  
		Size: 89.1 MB (89091280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b236848779e8b782bbd7b774ceb26a8d97926209e0e73fb8eec7dcc710956a6`  
		Last Modified: Wed, 11 Jun 2025 08:47:59 GMT  
		Size: 69.4 MB (69391179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6073936337a6273445e8e572628729d0f7c87e6b257269d88451a5f69af3976c`  
		Last Modified: Wed, 11 Jun 2025 08:47:35 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c59948a2223077e251c252d19ab2bdc1bc18471c561db52f3b42e2c0dd2e05ce`  
		Last Modified: Wed, 11 Jun 2025 08:47:40 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-1.12.1.1550-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:dad7ce33b290ef60e3d1b7d472a4e80c56dd7c93d5e6a136ed35026b1411ce2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5082282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f056565f4c13950c159f92d83ab9013fd96c30f0915be02dcddc92e3ea86752`

```dockerfile
```

-	Layers:
	-	`sha256:b48bd69ceac100a93e348de8147976594cbb02ba5763f3687b4bc5a879755358`  
		Last Modified: Wed, 11 Jun 2025 09:40:54 GMT  
		Size: 5.1 MB (5066292 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8ab40d375802188955793b11252def958457909ddf7e75c11fa88cd0083a007`  
		Last Modified: Wed, 11 Jun 2025 09:40:54 GMT  
		Size: 16.0 KB (15990 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-1.12.1.1550-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:9b97608b509248b5c1ad1d3b1a096879cdb645e573927c8b58dbc6b28ff3693f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.3 MB (197339757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:076f5598bafda5e9e45f0dbbe6a8104a9d578be0a3b3d580c11043624341fc45`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1749513600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c9cd5d5c131a8141631d87d9507a82e0549a2144689442301c07d2da80f39d19`  
		Last Modified: Tue, 10 Jun 2025 23:58:45 GMT  
		Size: 32.1 MB (32072795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd1482d1a6a9bdc5546550a2276353d49025aa1401c09bd7190a450152ac6579`  
		Last Modified: Wed, 11 Jun 2025 08:54:06 GMT  
		Size: 89.9 MB (89920261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcb42f6525853357ea6f6023481de7c731fdde76051a913c81df24f26de8f0d9`  
		Last Modified: Wed, 11 Jun 2025 09:00:18 GMT  
		Size: 75.3 MB (75345661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dee35299ef78d264d1920484a59d011c3023386eb012a2d4ed9daf936b6cdf3`  
		Last Modified: Wed, 11 Jun 2025 09:00:06 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ac4d173ecda932a90415eab0fbb1045b27271ef7eb95716e68ac21facd77a46`  
		Last Modified: Wed, 11 Jun 2025 09:00:07 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-1.12.1.1550-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:9c51fce7d1f48035462f78391414d25ff15db352b5dd0d1bbb36caf5b7d42472
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5082910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87698a9b22d7da8daaf60b677e636b2f9bae5921a60e8cf9b953c1d5f531c172`

```dockerfile
```

-	Layers:
	-	`sha256:d13f55453dbc648c6f4dac21d0e3144e2d652bdca873852a790aff3e3dc6cd5c`  
		Last Modified: Wed, 11 Jun 2025 09:40:59 GMT  
		Size: 5.1 MB (5066990 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76b883b4d19dd44acef2ae537d66997a1f587b76ab57d0cdb7a606a418628533`  
		Last Modified: Wed, 11 Jun 2025 09:41:00 GMT  
		Size: 15.9 KB (15920 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-1.12.1.1550-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:986490256739f96b29dd11ae0aa4eb932816421e107b4b1d1e09ef857a252815
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.4 MB (180439692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b113f89ff6c835dd810e1524925731ad55c5bebd1a421bcdbcf444a50b682c6e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1749513600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0f8692aee2900a8d946bd57522757b4d5de83b6af52eb0aa55e05d787a077615`  
		Last Modified: Tue, 10 Jun 2025 23:56:06 GMT  
		Size: 26.9 MB (26887853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8beb3c40ad9a8f7853b6aad4294e36a7e9ed2feae15a0ad9ca2e76019734aee6`  
		Last Modified: Wed, 11 Jun 2025 12:18:50 GMT  
		Size: 85.2 MB (85216766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4e8908e0273806043d2bcc6a3db7c7b5b1f52b1594555d466b44559927c0d17`  
		Last Modified: Wed, 11 Jun 2025 12:19:02 GMT  
		Size: 68.3 MB (68334029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db6a6466325ecd981934990f3b7830f3b6e44751be37581194bb8ee42c949fab`  
		Last Modified: Wed, 11 Jun 2025 12:19:06 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c37c6e5bcca50b436ae2f55cca61d601ba55850e13053cc953384b403894168`  
		Last Modified: Wed, 11 Jun 2025 12:19:07 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-1.12.1.1550-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:159e2a986e392001ffe4ca902ae902aa9c8523521e188dd154a6109a143d930b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5070275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39e8d00f31349cb9c4f3f509339c2a0ce2000aa2d103a566e3c72f2f1445067a`

```dockerfile
```

-	Layers:
	-	`sha256:dc3bd9ee237c34a9107c70abbcc2c843806cbd742c30b2127a78fbd211ff8f74`  
		Last Modified: Wed, 11 Jun 2025 06:38:52 GMT  
		Size: 5.1 MB (5054403 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4786b1799ec41704d238ccab516c2984d37ace05e6d8b45051e2f5de70db2d1`  
		Last Modified: Wed, 11 Jun 2025 06:38:53 GMT  
		Size: 15.9 KB (15872 bytes)  
		MIME: application/vnd.in-toto+json

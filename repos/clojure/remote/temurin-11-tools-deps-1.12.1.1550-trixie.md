## `clojure:temurin-11-tools-deps-1.12.1.1550-trixie`

```console
$ docker pull clojure@sha256:73a464bbbfc5d806c2e9443b64ba0b3aaf563d26842709d6444d1c541c1c1972
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

### `clojure:temurin-11-tools-deps-1.12.1.1550-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:f1e6c03a2dd78fa85b84412e487fa042d9ab71fe0c10ea698140df9432160745
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.2 MB (280155432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb1c29bd4efa8a18aefefebcc452933fe48f79564e3430b3220c29324e131add`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1749513600'
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
CMD ["clj"]
```

-	Layers:
	-	`sha256:d8e51f6b7dcdaee60f07f9a13a971abe1be9dc977d52d0849087118f80a1c7d6`  
		Last Modified: Tue, 10 Jun 2025 23:25:45 GMT  
		Size: 49.3 MB (49253859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e276e48228457a29aed7d098606796a5020b4a6bd5e45d8c3f3d6c9141c72200`  
		Last Modified: Wed, 11 Jun 2025 04:21:01 GMT  
		Size: 145.6 MB (145635595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fe7cfe902916b644abd3a61747f41ecc81aba901e8b00df009a14201ca8feb0`  
		Last Modified: Wed, 11 Jun 2025 00:13:51 GMT  
		Size: 85.3 MB (85265331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:339e2f387b7c18657a1f4a2af9153a0c219c0d8e078c1b434af103d2f4feee19`  
		Last Modified: Wed, 11 Jun 2025 00:13:46 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.1.1550-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:77d583c8565f6942592c3f069b22786f7c1dde99ed644103277cd57ba5378efe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7493518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5653e398a9d12a42f27ba4a67ff816532597e67df2494ba53c54b660857982a`

```dockerfile
```

-	Layers:
	-	`sha256:20c17e8c5a6199fd27b715b1ba47044cd20a4c7839af5ae98f45ac8c2616bede`  
		Last Modified: Wed, 11 Jun 2025 03:36:12 GMT  
		Size: 7.5 MB (7479290 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36b6cec5be3b3f9e8394746080d215fa0f6478ef848e32b4bbd84d762279d6a1`  
		Last Modified: Wed, 11 Jun 2025 03:36:13 GMT  
		Size: 14.2 KB (14228 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.1.1550-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:190f84204848da244c3779a9d524a33cb123232478efcf6b36031115ae892bcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.6 MB (280550610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:825446fae614c071e58a57f421017caa7de48b7de580619e5a7bd34df538baa6`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1747699200'
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
CMD ["clj"]
```

-	Layers:
	-	`sha256:397826b9fe635f12caff1a603eb12c37426a5b3dc563e0adff2debff0c68a6b0`  
		Last Modified: Tue, 03 Jun 2025 13:47:15 GMT  
		Size: 49.6 MB (49618294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6427a95fab6810b7c6cdb6297a4f0e9dd4a6bc046279a099df2fde01100b9e9b`  
		Last Modified: Fri, 06 Jun 2025 13:09:02 GMT  
		Size: 142.4 MB (142420666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc99c04ef26183ff92bf5d613e0ef2496f9f1b0eaa96c8a84aeda22aea69e82e`  
		Last Modified: Mon, 09 Jun 2025 17:44:07 GMT  
		Size: 88.5 MB (88511006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e34226b5caa5d3c1f210a39a0f08b20522b0a4bdbcade96b3729593e713ef088`  
		Last Modified: Mon, 09 Jun 2025 17:43:53 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.1.1550-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:6b5c46997eea88014929e98ad6fb0480d3e385db6ea2b7fb64e74d9784bb94cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7500770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de4b895e3ca19cb17a2bec360d6e98c9d7c82cff78c0e5218b634b4afcf1fee7`

```dockerfile
```

-	Layers:
	-	`sha256:927c3919406a5e85a185ec449adf2d195de63e30e657346707c57ace3ea39a86`  
		Last Modified: Mon, 09 Jun 2025 18:36:20 GMT  
		Size: 7.5 MB (7486424 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:014b2550867c6a950f8ea538c42f743b2069d0712e8d12efa491c541567b5371`  
		Last Modified: Mon, 09 Jun 2025 18:36:21 GMT  
		Size: 14.3 KB (14346 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.1.1550-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:4b87af726fe34aba2c1c85f4b9a0f5b2e5dc9b21c58620f5fb98fcaf9b59a898
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.8 MB (279842254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f9d19a391fb4469e54743d7b09a9ce68836f5ef934477c1730d317d478f93cd`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1747699200'
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
CMD ["clj"]
```

-	Layers:
	-	`sha256:25dfffa4126a91eb76c700c90bfdc9a9e15f34c7438a81f16c8a6999bbde6e45`  
		Last Modified: Tue, 03 Jun 2025 15:03:14 GMT  
		Size: 53.1 MB (53080544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39291d7ae4a9e82fc2c95d75539cc21cd0bc9715c3ac4d5b032793f128324bb4`  
		Last Modified: Mon, 09 Jun 2025 19:51:20 GMT  
		Size: 132.8 MB (132810533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14501d071f855d28b49eac95adfb1c9f989fd7682d8bd72945edf69836f2eb62`  
		Last Modified: Mon, 09 Jun 2025 17:57:04 GMT  
		Size: 94.0 MB (93950535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:948225a6454ea0cba7de833a7d8c3d32fd570d2261713fa9e5915e3c74f1d9b3`  
		Last Modified: Mon, 09 Jun 2025 17:57:00 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.1.1550-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:fe598f8c9d10dcca8a6b52daa5cb5b0776f0f5ada666acf71b85149469c26d62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7496854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3448abd2bc2bb1ade90e96a705429db5ab36bad0aa2d28198beb5e93acace88e`

```dockerfile
```

-	Layers:
	-	`sha256:a4aa106a123c97990684525093c0c168a7bb6f07594697aeb7ef11f346b8bb8f`  
		Last Modified: Mon, 09 Jun 2025 18:36:27 GMT  
		Size: 7.5 MB (7482578 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4368d829d895e5c745df7432092a30c7be11c3e51a82598207d28e4592b2f9a1`  
		Last Modified: Mon, 09 Jun 2025 18:36:28 GMT  
		Size: 14.3 KB (14276 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.1.1550-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:45f4cd9d0d8dc66e65395d5ecdbbad75e0b7968236e4e55505be286d934b3be4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.9 MB (263863767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e42b982009c621343fb0379a474db2cfd12bf247b0560cf463f1de9457a4c02a`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1747699200'
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
CMD ["clj"]
```

-	Layers:
	-	`sha256:71c8524b25c34592c256fbae9045d0ade48f5e9889d37c5b2190092fa9017d48`  
		Last Modified: Tue, 03 Jun 2025 15:34:07 GMT  
		Size: 49.3 MB (49322227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3809b7d5c48c969004e20fea95a6f198fb053f68fc077ceacfe71f6d2bf50ddd`  
		Last Modified: Tue, 10 Jun 2025 11:57:07 GMT  
		Size: 125.6 MB (125585319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dbc513e1590b987912a39b08647871df3695fb91952ce2a3bb403ccc6559648`  
		Last Modified: Tue, 10 Jun 2025 11:57:21 GMT  
		Size: 89.0 MB (88955576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a144cb0fc3cdd9385e9130c2fa1255e0cd5e19f4dada95141b3f137d97c2708c`  
		Last Modified: Mon, 09 Jun 2025 18:53:26 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.1.1550-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:1425232da553b29eead9cd74d54b393d4b2e155e7c49c462219805f934a3f408
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7488930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1473decebf05cb2e5e5bf048684983addb2cb47fdcdeb24fb32042fd6f85e702`

```dockerfile
```

-	Layers:
	-	`sha256:1e64251acbbcba9d522492a264c3a94bc82c3edf7cb6b3eb48dc944236b69912`  
		Last Modified: Mon, 09 Jun 2025 21:35:33 GMT  
		Size: 7.5 MB (7474702 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b7557ef64245233383093e789bb9d41106a73f8631c20a339e6b23306944018`  
		Last Modified: Mon, 09 Jun 2025 21:35:33 GMT  
		Size: 14.2 KB (14228 bytes)  
		MIME: application/vnd.in-toto+json

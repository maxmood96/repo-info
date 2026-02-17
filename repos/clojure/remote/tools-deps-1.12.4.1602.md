## `clojure:tools-deps-1.12.4.1602`

```console
$ docker pull clojure@sha256:2a9406b6e19001d64a6285136506bd6f1d854a7208e30fb406e7d78e1bfab359
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

### `clojure:tools-deps-1.12.4.1602` - linux; amd64

```console
$ docker pull clojure@sha256:7851a88a201a452bc36b10bc7ce24adf5159fe7118382b4b62038acd13649c8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.9 MB (221889077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5c9482352245773517764a9c55a01520937b40de0311f571445d3981552382c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 17 Feb 2026 21:45:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 21:45:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 21:45:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 21:45:34 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 17 Feb 2026 21:45:34 GMT
WORKDIR /tmp
# Tue, 17 Feb 2026 21:45:48 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Feb 2026 21:45:48 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Feb 2026 21:45:48 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Feb 2026 21:45:48 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Feb 2026 21:45:48 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6bc9f599b3efabc64230fd3b969d7654fcd6c6c98ad7cf7470093fe85274a7fc`  
		Last Modified: Tue, 03 Feb 2026 01:13:20 GMT  
		Size: 48.5 MB (48481483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cf9d22af060040e6ac300c0f415bb921c929ab0f10b74de3c85a9a925ca2c45`  
		Last Modified: Tue, 17 Feb 2026 21:46:10 GMT  
		Size: 92.3 MB (92256281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd766a2a8893b0e32682aa58feef2a8d5a783535c820b1c06a51bda17f9c81ee`  
		Last Modified: Tue, 17 Feb 2026 21:46:09 GMT  
		Size: 81.2 MB (81150269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6316f83cc303572da96e9228d7acb061070cc3c855b456a84a75aa5d8b9ab2a`  
		Last Modified: Tue, 17 Feb 2026 21:46:06 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f896119e6a276c5bead781c0dcc74164ab00345677531085edbbc63ffd6bb2b0`  
		Last Modified: Tue, 17 Feb 2026 21:46:07 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.4.1602` - unknown; unknown

```console
$ docker pull clojure@sha256:f016060bee15e498c169f7abb30c5947452a2b8c001faabb4d50077c352f1ff9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7363958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c50fc1a918fa20b1830b32a4e4165e2ef90980fa7eff16a066eea87a48e9540a`

```dockerfile
```

-	Layers:
	-	`sha256:b2739fecf98b233b3f7124a603bb5dfba830815b42b6be2e18c18b686170ec6f`  
		Last Modified: Tue, 17 Feb 2026 21:46:07 GMT  
		Size: 7.3 MB (7346187 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a481bac21f6ff5b38ec5de705aba8093220acc298e9c3273be475ac911282346`  
		Last Modified: Tue, 17 Feb 2026 21:46:07 GMT  
		Size: 17.8 KB (17771 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.4.1602` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:ad37ca3485c0260de28ce21ba8359153f60bf1d6d3580a742b24b7078c6fc763
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.8 MB (220793542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c28da20e63be3e6510cc00a20f261428bf0c6aed7c6bd54518608cb7eb7cec06`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1769990400'
# Tue, 17 Feb 2026 21:45:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 21:45:38 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 21:45:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 21:45:38 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 17 Feb 2026 21:45:38 GMT
WORKDIR /tmp
# Tue, 17 Feb 2026 21:45:53 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Feb 2026 21:45:54 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Feb 2026 21:45:54 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Feb 2026 21:45:54 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Feb 2026 21:45:54 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:64e8f4c09e7ac936ecc3deb0e61613f653224c28b2e35fa9d8e6e11cbdb5f911`  
		Last Modified: Tue, 03 Feb 2026 01:13:22 GMT  
		Size: 48.4 MB (48365956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0330d742ed679dc07301b05884cd5c717ae6d9f0e827c204545474fe2a10cec`  
		Last Modified: Tue, 17 Feb 2026 21:46:16 GMT  
		Size: 91.3 MB (91288277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a151dd7bb48f5aec8eaf06c86c0f780e07d69ed4cd349477b1d71654b03f1081`  
		Last Modified: Tue, 17 Feb 2026 21:46:16 GMT  
		Size: 81.1 MB (81138264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1cb677b16d22eedb1c36503c99117d431b6e1c4084b4175a0c831f5525a4840`  
		Last Modified: Tue, 17 Feb 2026 21:46:13 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:781e6f117ef21679e2ea4924d1bf7478915f1f3759dfddec354e957000e4a25e`  
		Last Modified: Tue, 17 Feb 2026 21:46:13 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.4.1602` - unknown; unknown

```console
$ docker pull clojure@sha256:58374040f032e1f6d2fd6b9d6842548e153703be57dc6d7e58a4dd8206706fdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7369980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f9c9accb59213033a8d3092a3306c686e6c3afeca6def4a91d7424db898d902`

```dockerfile
```

-	Layers:
	-	`sha256:0ca22b13460363856af12832a6fecbde2a58c0656de27e063533bf5c9e7c6a5b`  
		Last Modified: Tue, 17 Feb 2026 21:46:13 GMT  
		Size: 7.4 MB (7352019 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d8fc1158aa0c56c48c1cb513b72a1a9b8282ebd0f9f62a3f83df9e8f5d1c495`  
		Last Modified: Tue, 17 Feb 2026 21:46:13 GMT  
		Size: 18.0 KB (17961 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.4.1602` - linux; ppc64le

```console
$ docker pull clojure@sha256:be211f88d525e33c38a4c2181e18519417e2478fb6c5cdecf5369975383d9e7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.9 MB (230948403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:013035f48441564da0716e6492aaf8eba05226dd57480f94a56ce3f641f6809f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1769990400'
# Thu, 05 Feb 2026 23:54:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 23:54:17 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 05 Feb 2026 23:54:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 23:54:17 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Thu, 05 Feb 2026 23:54:18 GMT
WORKDIR /tmp
# Fri, 06 Feb 2026 00:51:14 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 06 Feb 2026 00:51:15 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 06 Feb 2026 00:51:16 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 06 Feb 2026 00:51:16 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 06 Feb 2026 00:51:16 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:5e189aacb842725e8d1d9877c9ab9af09e14901412b6665e179393112b5bca51`  
		Last Modified: Tue, 03 Feb 2026 01:12:57 GMT  
		Size: 52.3 MB (52327289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:413bd0b8c6c326da16c676c4dc2f9ba6260e745418e4f97b3a2d3fb7fa2bf0a6`  
		Last Modified: Thu, 05 Feb 2026 23:57:00 GMT  
		Size: 91.6 MB (91632873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ff49bdb92c29d1aa0a5728614463126c1cb70700342bdd4563bf11bcb84f9c5`  
		Last Modified: Fri, 06 Feb 2026 00:52:01 GMT  
		Size: 87.0 MB (86987198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7846677a8fe0a48bbcf1c1e4fdeb070ff23256f19e07d916a49d6ce8dbd9402`  
		Last Modified: Fri, 06 Feb 2026 00:51:58 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:071f8bfc37cc85641a427ac9f96190881bc3f500b3a164f6dda5b316b54df8e1`  
		Last Modified: Fri, 06 Feb 2026 00:51:58 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.4.1602` - unknown; unknown

```console
$ docker pull clojure@sha256:8bf9f3dd13dcd9b1cf34a268c8fbfb71d14fedc3aadeb9507a6972de6e441f45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7352606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67ae5eb937ed2d77facbe36eb82bfabc735e65bc8082befc5c101899789e6458`

```dockerfile
```

-	Layers:
	-	`sha256:a3c93014ea6d741e92c574384cf26c04b52604509e6e93a28f9c1efc1e6b0787`  
		Last Modified: Fri, 06 Feb 2026 00:51:58 GMT  
		Size: 7.3 MB (7334751 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b69d8d447aa3ac62ca3180a6ba618b9cd9a7017491531116fa05b2ae459379a2`  
		Last Modified: Fri, 06 Feb 2026 00:51:58 GMT  
		Size: 17.9 KB (17855 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.4.1602` - linux; s390x

```console
$ docker pull clojure@sha256:b01e877fcccebc0b3603cef0974ade8915d70cf27da03b06ae9d995b7ca32599
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.3 MB (215336333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90f0e96aeac35f60d6ee3e6c1d9fbcef047e0daa15462d355f42ec68786e9ddf`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1769990400'
# Thu, 05 Feb 2026 23:08:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 23:08:00 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 05 Feb 2026 23:08:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 23:08:00 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Thu, 05 Feb 2026 23:08:00 GMT
WORKDIR /tmp
# Thu, 05 Feb 2026 23:09:22 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 05 Feb 2026 23:09:22 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 05 Feb 2026 23:09:22 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 05 Feb 2026 23:09:22 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 05 Feb 2026 23:09:22 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:4c4c4621da5085342b3b0d8d8ef57e5e44004eedf5818268af30c41a02cb6cf2`  
		Last Modified: Tue, 03 Feb 2026 01:12:48 GMT  
		Size: 47.1 MB (47138343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35eccc4f13414ab485daaa590101b622dee874ce7e0938b87911ff71b39f8ce2`  
		Last Modified: Thu, 05 Feb 2026 23:08:43 GMT  
		Size: 88.2 MB (88233820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9831ee652926ca839320573d9de5e5c26e5acce19f66e74c3871290e7fe30e0a`  
		Last Modified: Thu, 05 Feb 2026 23:09:50 GMT  
		Size: 80.0 MB (79963129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab6b664ddd32574ffc081b02edaa95a7d5998648036f47aef7c092c99c2135ba`  
		Last Modified: Thu, 05 Feb 2026 23:09:48 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eca0747ea95d29defb9392338ef98686b00faba8d39cb5133fb504a860f6aca`  
		Last Modified: Thu, 05 Feb 2026 23:09:48 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.4.1602` - unknown; unknown

```console
$ docker pull clojure@sha256:f57c6ac811fb0ff2c2caa22b4a8a7d7fcf89dc08f9074816026ad70d2b71c23d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7339839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2f9eca333f2dbe08308aa8e583eb0a137f9b6be8516e39edf6a5749a06861b4`

```dockerfile
```

-	Layers:
	-	`sha256:e07ccb085c27368bf29edf41802abbdf61b9c00bdda39c9d6b5a7fa0eb85b2c2`  
		Last Modified: Thu, 05 Feb 2026 23:09:48 GMT  
		Size: 7.3 MB (7322068 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a5ed5f9f80d395183745a48006e3cdcbe15cacf8a39b5ed76ffded2cfb42bba`  
		Last Modified: Thu, 05 Feb 2026 23:09:48 GMT  
		Size: 17.8 KB (17771 bytes)  
		MIME: application/vnd.in-toto+json

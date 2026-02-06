## `clojure:temurin-25-bookworm`

```console
$ docker pull clojure@sha256:206100534e98f78963a476a7faa1a429607834acd3dcb268b4b635b2d68f589a
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

### `clojure:temurin-25-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:ff6faaa1e5d3c1addb97c8bd0f36dac549d1a53e0e6d8cd4f6f9274a9de68fe1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.9 MB (221889880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd7f0bc1e7c98cf0ad54fc5ae8653877c0cac63be58942587d2b452a53206913`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Thu, 05 Feb 2026 23:07:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 23:07:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 05 Feb 2026 23:07:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 23:07:12 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Thu, 05 Feb 2026 23:07:12 GMT
WORKDIR /tmp
# Thu, 05 Feb 2026 23:07:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 05 Feb 2026 23:07:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 05 Feb 2026 23:07:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 05 Feb 2026 23:07:26 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 05 Feb 2026 23:07:26 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6bc9f599b3efabc64230fd3b969d7654fcd6c6c98ad7cf7470093fe85274a7fc`  
		Last Modified: Tue, 03 Feb 2026 01:13:20 GMT  
		Size: 48.5 MB (48481483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4391e0dc81b0b4cf189b4cd1e37b829b0485e4e51490ed01845c841da6b11b4c`  
		Last Modified: Thu, 05 Feb 2026 23:07:49 GMT  
		Size: 92.3 MB (92256283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f6d0cb3c7354a4a8422dcf59d29b87407b868beb07858cb3c82975771d9dba2`  
		Last Modified: Thu, 05 Feb 2026 23:07:49 GMT  
		Size: 81.2 MB (81151072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9de22912607829713bd6100f9e7ba4088ae5c063373dbf095caf489e2db08bb`  
		Last Modified: Thu, 05 Feb 2026 23:07:46 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:360f5408faa0217b398896531a58967339b9e2f64740ccdeb8c5f64c3d5e6435`  
		Last Modified: Thu, 05 Feb 2026 23:07:46 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:4f390650fbf1ceaf43c0b7fb2ab866dc8a86859f49032f127247ce70d2d398f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7363958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96528483586146379ed75ff7bf7bf5302527a9f74fba3d7af1a0167f0e234817`

```dockerfile
```

-	Layers:
	-	`sha256:7c6fcb9a9ee8f98da975654bd9a2a1436d46076a5b8600f5dbe3bb0ac84a9349`  
		Last Modified: Thu, 05 Feb 2026 23:07:46 GMT  
		Size: 7.3 MB (7346187 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2beef745029e1de9d237d0c231d6f057b6767779f1c70a7739368de291e75bd6`  
		Last Modified: Thu, 05 Feb 2026 23:07:46 GMT  
		Size: 17.8 KB (17771 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:cb7d5a961ae2638e7a7012cb7aaca0390e1a9757f3aeaa568e279422c135acc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.8 MB (220793864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c87cb9a2b586a24a9406014ce982706e3220fcd34ee3b6c4e36ef46d8c07c3a3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1769990400'
# Thu, 05 Feb 2026 23:08:30 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 23:08:30 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 05 Feb 2026 23:08:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 23:08:30 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Thu, 05 Feb 2026 23:08:30 GMT
WORKDIR /tmp
# Thu, 05 Feb 2026 23:08:45 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 05 Feb 2026 23:08:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 05 Feb 2026 23:08:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 05 Feb 2026 23:08:46 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 05 Feb 2026 23:08:46 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:64e8f4c09e7ac936ecc3deb0e61613f653224c28b2e35fa9d8e6e11cbdb5f911`  
		Last Modified: Tue, 03 Feb 2026 01:13:22 GMT  
		Size: 48.4 MB (48365956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61a99187bc37f4ee8a2b7ea24ea3d3819b41db9751d4e889b6a11a0ffbd2d18f`  
		Last Modified: Thu, 05 Feb 2026 23:09:10 GMT  
		Size: 91.3 MB (91288252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6af8edad326d308adde9ba06456df8926c0a99290af578822177a851d4772dbd`  
		Last Modified: Thu, 05 Feb 2026 23:09:10 GMT  
		Size: 81.1 MB (81138612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0da9cb0db26ca21800ccb9267ace505c8ad473170b2c2aaa5d0f5f2a3f6ff37`  
		Last Modified: Thu, 05 Feb 2026 23:09:05 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0250e90d92d96c7741cb340deb4545889fcdefeac9f3d9f4fa9e82356b90cf3a`  
		Last Modified: Thu, 05 Feb 2026 23:09:05 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:8454e27d6cfc1148aca55a753aa9ca73fcc3830a9776c0e29c8a6187df5d5634
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7369980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4903ac15a67a55b90a480e6f5f0bac95eec166584b51cb451edd50d51cd10263`

```dockerfile
```

-	Layers:
	-	`sha256:fd2f907164cc5349cc61093343951b52ef1521ff5435a43db58976c7d326ac13`  
		Last Modified: Thu, 05 Feb 2026 23:09:06 GMT  
		Size: 7.4 MB (7352019 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58101d195ef07020fdf07ab3fd59c0cbcdaa2dd27b7f943855a6b92abf734318`  
		Last Modified: Thu, 05 Feb 2026 23:09:05 GMT  
		Size: 18.0 KB (17961 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-bookworm` - linux; ppc64le

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

### `clojure:temurin-25-bookworm` - unknown; unknown

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

### `clojure:temurin-25-bookworm` - linux; s390x

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

### `clojure:temurin-25-bookworm` - unknown; unknown

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

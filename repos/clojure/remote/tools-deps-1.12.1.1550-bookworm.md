## `clojure:tools-deps-1.12.1.1550-bookworm`

```console
$ docker pull clojure@sha256:dda85dee8f3da93cdea8dd1d3dd3ddec76c69481c6e0e98ec9177d6c17c73653
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

### `clojure:tools-deps-1.12.1.1550-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:8778c785ad3cab8a62ec59dcd0646f1b3d3285251938f38e35e5d2d4b9e8e15d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.1 MB (287123694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c6708e0efef835febeb44ba004dab438b648c41772a2227d51f24e53813589c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1749513600'
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
	-	`sha256:0c01110621e0ec1eded421406c9f117f7ae5486c8f7b0a0d1a37cc7bc9317226`  
		Last Modified: Tue, 10 Jun 2025 22:46:22 GMT  
		Size: 48.5 MB (48494272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:560d6869f1e9555211af069114a3a0030cef0fae77bc7e1844367eb06fed90bd`  
		Last Modified: Wed, 11 Jun 2025 03:42:34 GMT  
		Size: 157.6 MB (157634484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b4655b1fd4ec67f3c92fd6ef7fdb3b5871b3c99bdb2f96e906086c3e6bebdb9`  
		Last Modified: Tue, 10 Jun 2025 23:52:58 GMT  
		Size: 81.0 MB (80993900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:054b84ab6abada3cbf0e97a3eba2c658f694b9df7dd38a8d4079c857ea6d6341`  
		Last Modified: Tue, 10 Jun 2025 23:52:51 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c0813763ffeb0f43c090569db7315416a26ffe27c20e308c8d44fb6fc651d07`  
		Last Modified: Tue, 10 Jun 2025 23:52:51 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.1.1550-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:eadffaca318a0ebe714cc4c0ca964dc2146886459103a7e684b65105f6f881dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7389835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:940e4fac834a50585edeb976c58e63d286903f86dc614e3416d00ac5e2127a7e`

```dockerfile
```

-	Layers:
	-	`sha256:7a1b96ea1ce48b5d1ec32958c9b0071a7d72e6fd5166a9b0c1c30a4f46030a61`  
		Last Modified: Wed, 11 Jun 2025 03:38:13 GMT  
		Size: 7.4 MB (7372014 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f5a56d25449f6d063a90f3dcb945f6f740f97017854e907077b25ab87e667df`  
		Last Modified: Wed, 11 Jun 2025 03:38:14 GMT  
		Size: 17.8 KB (17821 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.1.1550-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:9f2841492bc2a78d4f1fd18e2ad8c6488ba7e6c5bffa35b8864e72e8c44f4a15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.1 MB (285105433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83d2be68f20f2b8921d12753de69cb433a6302f362e359e5bf5c7b2a4bdda543`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
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
	-	`sha256:1a12b4ea7c0ce04aa0e98be0a8c9942162bac71426f734fe6d3bf988bc9e2627`  
		Last Modified: Tue, 03 Jun 2025 13:30:16 GMT  
		Size: 48.3 MB (48327181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:437f8f7a50b2952398084c7b3ca28b3cfe6e72e05419b0e1b568927135d80a2d`  
		Last Modified: Tue, 03 Jun 2025 13:43:18 GMT  
		Size: 155.9 MB (155928814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc56d3d10045d4b80aad14367c0bba9da6bf23ec008de1ea2f71d8cadfa23577`  
		Last Modified: Mon, 09 Jun 2025 17:52:08 GMT  
		Size: 80.8 MB (80848398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d12cfdd202cbef614fa13b0585d78f42db8d32b3ae4fdf52ea5a585824b625c0`  
		Last Modified: Mon, 09 Jun 2025 17:51:59 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c29a9e81dad7c0101024863e951557744f7b0f3d09e644f565f8e25ac38ff23`  
		Last Modified: Mon, 09 Jun 2025 17:51:58 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.1.1550-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:de60972c32bb46258cde5cb3534298b63305c07a88ff85ddad51cfbd77086bac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7395860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64b6efd9c5e1b47e2e06ec0271008f815cf77a1059fa9944e3adf54edca57e1d`

```dockerfile
```

-	Layers:
	-	`sha256:d9e87165dcc4b7d405aef5b84301cfb8693b72826628b80f172e08495fab287f`  
		Last Modified: Mon, 09 Jun 2025 18:39:07 GMT  
		Size: 7.4 MB (7377849 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5e33394a2a781bbe7eef1dd6533a04127b19c9134929ea1bbfc8d8dacbe46b4`  
		Last Modified: Mon, 09 Jun 2025 18:39:08 GMT  
		Size: 18.0 KB (18011 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.1.1550-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:32088479daa841a6aee0cf70b1022f58c5534a7a09da5c0e6a4248b05f45b961
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.0 MB (296950988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:124b545b706585f813a1544ba7e98ee0562b68b12aaec31c4b463fa593a041a5`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1747699200'
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
	-	`sha256:996840ee350796081b3c80118ca1a58ce8212c6fdf88c454706a16457903a0c9`  
		Last Modified: Tue, 03 Jun 2025 13:33:40 GMT  
		Size: 52.3 MB (52331619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:860dcfb7182a5dc32b212ca727ac1ab0a7e7f5698fd7540ceb4c7f84c97337da`  
		Last Modified: Mon, 09 Jun 2025 03:22:39 GMT  
		Size: 157.8 MB (157804869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:343ae8cef8e12d2af44b1b62d7c140751e2f60942b96e3914ceac3c1a2c41ef1`  
		Last Modified: Mon, 09 Jun 2025 18:11:19 GMT  
		Size: 86.8 MB (86813457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00a74502f76ea04e67e70441fe5b18368f3ae5944b7e85a00746928398a3e8aa`  
		Last Modified: Mon, 09 Jun 2025 18:11:10 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0089c96883885602ebb29facce2302fcbba625b3f6c84a4ae82a3d2d26b86286`  
		Last Modified: Mon, 09 Jun 2025 18:11:10 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.1.1550-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:82d6a542af54c7e17f4ee4a8a9398e87e4f146b04f292f43628f5da12ea072e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7395159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30614ee91cd78aaa5845cf934a422cb5914c62fc07eb168cb0d0bda99675658f`

```dockerfile
```

-	Layers:
	-	`sha256:03b192c1179a03a0629fb9f22e3402312bc100ca57c96f51d122cbc689877415`  
		Last Modified: Mon, 09 Jun 2025 21:37:25 GMT  
		Size: 7.4 MB (7377254 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee9650792ef0aad6cbcd80d2aec295733b37bf88ed11cf82fbbb645923abbddb`  
		Last Modified: Mon, 09 Jun 2025 21:37:26 GMT  
		Size: 17.9 KB (17905 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.1.1550-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:e746db3e22716327864e65059deb60a1eb8a63fcbe94eabf449d0f7d08f59cc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.9 MB (273864088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21a4ba8284bc4f69d55e63959acd1c91972b2909555aef52d9f70fafb7702d8f`
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
	-	`sha256:92d876c60c42d9677caf30587cba2266fe6860ddc50efdd0a6fcec154e589f76`  
		Last Modified: Tue, 10 Jun 2025 22:48:13 GMT  
		Size: 47.1 MB (47149408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bda1d40bcba3d4c5b290c8a74ba0b4bfc95975ec2a23ad75658cd28e277e6baf`  
		Last Modified: Wed, 11 Jun 2025 07:02:00 GMT  
		Size: 146.9 MB (146911003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00daefb7d687a91e318b16b9c1b635a7bd53f6349d4a75495f9ef6c8a30fe7f6`  
		Last Modified: Wed, 11 Jun 2025 07:02:07 GMT  
		Size: 79.8 MB (79802636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54535089bc5a0ebd19412f776b37612e1336fbf15d98b201ced1736703e3d6e4`  
		Last Modified: Wed, 11 Jun 2025 05:53:58 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fe0e2775354ef3c08ec3d2ee064a0cb638c1ab001835e39d2f7a6333ff2f5c5`  
		Last Modified: Wed, 11 Jun 2025 05:54:03 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.1.1550-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:a1354e245c8517863555a852e32673fb76796cf554b6696f80f6bf9c3ef3db0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7381153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4cdaa4075dd3749f34df080f725d6278a930315a1b7a2586190963a629aa3e1`

```dockerfile
```

-	Layers:
	-	`sha256:264c52cddfdb2eb5e0cc6dfe35676f31cf5fe29e9bea5595966b60cf9e888c08`  
		Last Modified: Wed, 11 Jun 2025 06:37:41 GMT  
		Size: 7.4 MB (7363333 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:07a67f6c9f91024a09aa321cd16c1eb882ab93d3fd2c149954f9820c8bb8fcfb`  
		Last Modified: Wed, 11 Jun 2025 06:37:42 GMT  
		Size: 17.8 KB (17820 bytes)  
		MIME: application/vnd.in-toto+json

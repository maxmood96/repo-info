<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `kibana`

-	[`kibana:6.8.12`](#kibana6812)
-	[`kibana:7.9.1`](#kibana791)

## `kibana:6.8.12`

```console
$ docker pull kibana@sha256:b82ddf3ba69ea030702993a368306a744ca532347d2d00f21b4f6439ab64bb0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kibana:6.8.12` - linux; amd64

```console
$ docker pull kibana@sha256:6b4d3c1a8b6e3eaaedfd3d81637a273877355b17938f41954f46fcaba788b756
```

-	Docker Version: 19.03.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.8 MB (275759911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4227d845381f42d8884c0fe00099691efe653d6679976a632ed66410a935c9de`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Mon, 10 Aug 2020 18:20:08 GMT
ADD file:61908381d3142ffba798ae9a904476d19b197ab79d0338f14bec0f76649df8d4 in / 
# Mon, 10 Aug 2020 18:20:09 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20200809 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-08-09 00:00:00+01:00
# Mon, 10 Aug 2020 18:20:09 GMT
CMD ["/bin/bash"]
# Wed, 12 Aug 2020 08:18:33 GMT
EXPOSE 5601
# Wed, 12 Aug 2020 08:18:46 GMT
RUN yum update -y && yum install -y fontconfig freetype && yum clean all
# Wed, 12 Aug 2020 08:19:32 GMT
COPY --chown=1000:0dir:aaf12d5b2b623394c1178c4c2bb82e74abe0db0ddb95a085c41446962b4a2fea in /usr/share/kibana 
# Wed, 12 Aug 2020 08:19:33 GMT
WORKDIR /usr/share/kibana
# Wed, 12 Aug 2020 08:19:38 GMT
RUN ln -s /usr/share/kibana /opt/kibana
# Wed, 12 Aug 2020 08:19:38 GMT
ENV ELASTIC_CONTAINER=true
# Wed, 12 Aug 2020 08:19:38 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Aug 2020 08:19:39 GMT
COPY --chown=1000:0file:60b6181f28c99b362092ea6139b6d4112ddd0bef32d52563c33b26bdc2b51318 in /usr/share/kibana/config/kibana.yml 
# Wed, 12 Aug 2020 08:19:39 GMT
COPY --chown=1000:0file:7d472d1939e23e2f10e7c5fd1e9166eefd646214aa0d8a1c09d92af71c9cbd87 in /usr/local/bin/ 
# Wed, 12 Aug 2020 08:19:42 GMT
RUN chmod g+ws /usr/share/kibana && find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \;
# Wed, 12 Aug 2020 08:19:44 GMT
RUN groupadd --gid 1000 kibana && useradd --uid 1000 --gid 1000 --home-dir /usr/share/kibana --no-create-home kibana
# Wed, 12 Aug 2020 08:19:44 GMT
USER kibana
# Wed, 12 Aug 2020 08:19:45 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.label-schema.name=kibana org.label-schema.version=6.8.12 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.license=Elastic License license=Elastic License
# Wed, 12 Aug 2020 08:19:45 GMT
CMD ["/usr/local/bin/kibana-docker"]
```

-	Layers:
	-	`sha256:75f829a71a1c5277a7abf55495ac8d16759691d980bf1d931795e5eb68a294c0`  
		Last Modified: Mon, 10 Aug 2020 18:21:46 GMT  
		Size: 75.9 MB (75863188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ae3692e2bce8770380160b51df0a5e91a2858ea47e542c9b973e93064b95356`  
		Last Modified: Wed, 19 Aug 2020 21:36:38 GMT  
		Size: 10.0 MB (9978517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:932a0bf8c03a6542c0ac8a560daaf7f752df4089bc798a2dde560ae30e37134f`  
		Last Modified: Wed, 19 Aug 2020 21:37:15 GMT  
		Size: 189.9 MB (189913467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6acea4293b251dff6ff3f3efa114856c0b2d0ef12ead303b45eefb5735bcfb09`  
		Last Modified: Wed, 19 Aug 2020 21:36:34 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bd647c0da003b3d0e5c904f7547c9f91ed7237654caa99af3079a59df7aae9c`  
		Last Modified: Wed, 19 Aug 2020 21:36:34 GMT  
		Size: 392.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c126949930cea80b9b663a44838654d557054de4765c5ccae77405623a6fe09`  
		Last Modified: Wed, 19 Aug 2020 21:36:34 GMT  
		Size: 2.3 KB (2257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1319ec5a92666214bb9da7dc210375a7c5366402545edf38aa035d4d78d57a1`  
		Last Modified: Wed, 19 Aug 2020 21:36:34 GMT  
		Size: 147.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37183b6c21cce0d08cda644ca1fc67ac1eee89721065b07a569d5548e52a5890`  
		Last Modified: Wed, 19 Aug 2020 21:36:34 GMT  
		Size: 1.8 KB (1811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kibana:7.9.1`

```console
$ docker pull kibana@sha256:b1bbcaa5773844cb75465031e20b3619bd631a4843a074e4f4a3a009e246c5d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kibana:7.9.1` - linux; amd64

```console
$ docker pull kibana@sha256:8ede5f956d1670b5cd446e0f48b31edcd53310cd03b0cd9116ea6009cd0b3d6f
```

-	Docker Version: 19.03.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **386.7 MB (386665107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f79360c362ee6d6920680381da103f1114d8ded2af8f0c3c2feb2718a62002b`
-	Entrypoint: `["\/usr\/local\/bin\/dumb-init","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Mon, 10 Aug 2020 18:20:08 GMT
ADD file:61908381d3142ffba798ae9a904476d19b197ab79d0338f14bec0f76649df8d4 in / 
# Mon, 10 Aug 2020 18:20:09 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20200809 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-08-09 00:00:00+01:00
# Mon, 10 Aug 2020 18:20:09 GMT
CMD ["/bin/bash"]
# Tue, 01 Sep 2020 22:42:31 GMT
EXPOSE 5601
# Tue, 01 Sep 2020 22:42:47 GMT
RUN yum update -y && yum install -y fontconfig freetype shadow-utils && yum clean all
# Tue, 01 Sep 2020 22:42:49 GMT
RUN curl -L -o /usr/local/bin/dumb-init https://github.com/Yelp/dumb-init/releases/download/v1.2.2/dumb-init_1.2.2_amd64
# Tue, 01 Sep 2020 22:42:52 GMT
RUN echo "37f2c1f0372a45554f1b89924fbb134fc24c3756efaedf11e07f599494e0eff9  /usr/local/bin/dumb-init" | sha256sum -c -
# Tue, 01 Sep 2020 22:42:55 GMT
RUN chmod +x /usr/local/bin/dumb-init
# Tue, 01 Sep 2020 22:44:02 GMT
COPY --chown=1000:0dir:986813b2cde16fd8e0d754221c8bb282c0fd24d00606f100439be003f892b7f2 in /usr/share/kibana 
# Tue, 01 Sep 2020 22:44:04 GMT
WORKDIR /usr/share/kibana
# Tue, 01 Sep 2020 22:44:07 GMT
RUN ln -s /usr/share/kibana /opt/kibana
# Tue, 01 Sep 2020 22:44:07 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 01 Sep 2020 22:44:07 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Sep 2020 22:44:09 GMT
COPY --chown=1000:0file:ea1f294356f14dfc1a50e3303613e69f187589962058569d5b3282460d7f28cb in /usr/share/kibana/config/kibana.yml 
# Tue, 01 Sep 2020 22:44:10 GMT
COPY --chown=1000:0file:49929e11929a90fcf66378d41dd877886d468312d3a58507814cd4315da06baf in /usr/local/bin/ 
# Tue, 01 Sep 2020 22:44:14 GMT
RUN chmod g+ws /usr/share/kibana && find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \;
# Tue, 01 Sep 2020 22:44:19 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} +
# Tue, 01 Sep 2020 22:44:23 GMT
RUN groupadd --gid 1000 kibana && useradd --uid 1000 --gid 1000 --home-dir /usr/share/kibana --no-create-home kibana
# Tue, 01 Sep 2020 22:44:23 GMT
USER kibana
# Tue, 01 Sep 2020 22:44:24 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.label-schema.name=kibana org.label-schema.version=7.9.1 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.license=Elastic License org.label-schema.usage=https://www.elastic.co/guide/en/kibana/index.html org.label-schema.build-date=2020-09-01T22:38:56.015Z license=Elastic License
# Tue, 01 Sep 2020 22:44:24 GMT
ENTRYPOINT ["/usr/local/bin/dumb-init" "--"]
# Tue, 01 Sep 2020 22:44:25 GMT
CMD ["/usr/local/bin/kibana-docker"]
```

-	Layers:
	-	`sha256:75f829a71a1c5277a7abf55495ac8d16759691d980bf1d931795e5eb68a294c0`  
		Last Modified: Mon, 10 Aug 2020 18:21:46 GMT  
		Size: 75.9 MB (75863188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad965601e373e489322f6bcc17941e385caf6c1a824fed6a0cafeb87f985cd12`  
		Last Modified: Thu, 03 Sep 2020 21:37:25 GMT  
		Size: 10.0 MB (9980250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6d9c1915b86c5563d18cc3a0c889d1ae6d6551c64ef9cd43d57817bf73bbfb2`  
		Last Modified: Thu, 03 Sep 2020 21:37:22 GMT  
		Size: 31.7 KB (31680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c81b6cd56958a281c5702287c242d6d59570f2638c01c3055e068a4bb0e0cf6`  
		Last Modified: Thu, 03 Sep 2020 21:37:22 GMT  
		Size: 30.2 KB (30193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dbf6007c4fd19bb998dc634d172a46bd119ebbc7255862fae0fb8322fcbd245`  
		Last Modified: Fri, 04 Sep 2020 20:28:25 GMT  
		Size: 300.6 MB (300553653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35d2bcbba4c3b816ce3270a864733e2277c25ceba43004462cd296c996d7f447`  
		Last Modified: Fri, 04 Sep 2020 20:27:34 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a22c1b07a6516d696be2e9195eb8fbe90eb4be15f423858cd001d46e7c48044`  
		Last Modified: Fri, 04 Sep 2020 20:27:33 GMT  
		Size: 383.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7882853946c07805c0787e7537b6adf2d1b85cdd877f5976d21c952f196392a`  
		Last Modified: Fri, 04 Sep 2020 20:27:33 GMT  
		Size: 3.0 KB (3049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2dba57c3dd6534c2e7bd31bc14c2f259eff871e66389010ff194b6129594456`  
		Last Modified: Fri, 04 Sep 2020 20:27:33 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e40ec53fd1bc84ad102e36398d48484de821b8e6ab029e025ad5a53d8ee1ea54`  
		Last Modified: Thu, 03 Sep 2020 21:37:19 GMT  
		Size: 200.6 KB (200611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0cc3aacd251553e365b83a5eaf378433fd1bfc3a02868a7f2e3543aea5f3f23`  
		Last Modified: Fri, 04 Sep 2020 20:27:33 GMT  
		Size: 1.8 KB (1818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

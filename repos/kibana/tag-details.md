<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `kibana`

-	[`kibana:6.8.10`](#kibana6810)
-	[`kibana:7.7.1`](#kibana771)

## `kibana:6.8.10`

```console
$ docker pull kibana@sha256:869d341dc243016903a6676bf0df584f609596db61c8795292cfda39efc4eae4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kibana:6.8.10` - linux; amd64

```console
$ docker pull kibana@sha256:64fdf609366005ecb4b3166c519142e09f5a3f98c72af6230cf9ff77aa3b60e1
```

-	Docker Version: 19.03.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.2 MB (287204827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37ba3ee8f03d2b0ff8078da24ae6b437b4675b6c7f9c3d3e05ea68fb33a90c3b`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Tue, 05 May 2020 21:20:06 GMT
ADD file:38e2d2a1a0cd8694bd5086f257fdf7504f0c2481bf4f746c9bd1c8d9f3f6430d in / 
# Tue, 05 May 2020 21:20:06 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20200504 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-05-04 00:00:00+01:00
# Tue, 05 May 2020 21:20:07 GMT
CMD ["/bin/bash"]
# Thu, 28 May 2020 15:43:06 GMT
EXPOSE 5601
# Thu, 28 May 2020 15:43:33 GMT
RUN yum update -y && yum install -y fontconfig freetype && yum clean all
# Thu, 28 May 2020 15:44:22 GMT
COPY --chown=1000:0dir:8dd346bef08bcc2914a80b92aff967dd2bc25f78f319095e1fd38f911f4ed149 in /usr/share/kibana 
# Thu, 28 May 2020 15:44:23 GMT
WORKDIR /usr/share/kibana
# Thu, 28 May 2020 15:44:26 GMT
RUN ln -s /usr/share/kibana /opt/kibana
# Thu, 28 May 2020 15:44:27 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 28 May 2020 15:44:28 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 May 2020 15:44:28 GMT
COPY --chown=1000:0file:60b6181f28c99b362092ea6139b6d4112ddd0bef32d52563c33b26bdc2b51318 in /usr/share/kibana/config/kibana.yml 
# Thu, 28 May 2020 15:44:29 GMT
COPY --chown=1000:0file:7d472d1939e23e2f10e7c5fd1e9166eefd646214aa0d8a1c09d92af71c9cbd87 in /usr/local/bin/ 
# Thu, 28 May 2020 15:44:32 GMT
RUN chmod g+ws /usr/share/kibana && find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \;
# Thu, 28 May 2020 15:44:34 GMT
RUN groupadd --gid 1000 kibana && useradd --uid 1000 --gid 1000 --home-dir /usr/share/kibana --no-create-home kibana
# Thu, 28 May 2020 15:44:34 GMT
USER kibana
# Thu, 28 May 2020 15:44:35 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.label-schema.name=kibana org.label-schema.version=6.8.10 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.license=Elastic License license=Elastic License
# Thu, 28 May 2020 15:44:35 GMT
CMD ["/usr/local/bin/kibana-docker"]
```

-	Layers:
	-	`sha256:524b0c1e57f8ee5fee01a1decba2f301c324a6513ca3551021264e3aa7341ebc`  
		Last Modified: Tue, 05 May 2020 21:23:14 GMT  
		Size: 75.9 MB (75880141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:995afa16ecfa406c5ea52654a094e30434e2fe3ef29501b38de2499f86dc7892`  
		Last Modified: Wed, 03 Jun 2020 14:43:20 GMT  
		Size: 26.7 MB (26694615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:349b1ac413c0a4cf5bc8f6d2162105597f93167adf2860cb48343f7585ade807`  
		Last Modified: Wed, 03 Jun 2020 14:46:29 GMT  
		Size: 184.6 MB (184625328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e2abce3f35d21da474640c8c2145662b2575e9eaaa187e9837a9bc0d37a237c`  
		Last Modified: Wed, 03 Jun 2020 14:45:55 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffcb1d18ee09be15c8c55f1ace4690145fe53601d19ea1476da07b953d27d571`  
		Last Modified: Wed, 03 Jun 2020 14:45:56 GMT  
		Size: 392.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b710880b79d8529f317c0ee5708c37b28b4909f8e6353ab2d8199e1841b0eb0d`  
		Last Modified: Wed, 03 Jun 2020 14:45:55 GMT  
		Size: 2.3 KB (2261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac16ab7d13ed0eda875267502eadea25df26f53ce81ee948930235a5c5436dab`  
		Last Modified: Wed, 03 Jun 2020 14:45:55 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c875a630bb8b3b24b054b2910e2f2665de38afacb9159b43a5103f80ef771da5`  
		Last Modified: Wed, 03 Jun 2020 14:45:55 GMT  
		Size: 1.8 KB (1809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kibana:7.7.1`

```console
$ docker pull kibana@sha256:ea0eab16b0330e6b3d9083e3c8fd6e82964fc9659989a75ecda782fbd160fdaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kibana:7.7.1` - linux; amd64

```console
$ docker pull kibana@sha256:53c0edc5671edb7ed17f939f27db21366cfb6be647499d934b4b5538baa315d0
```

-	Docker Version: 19.03.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **384.9 MB (384851219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6de54f813b39c0a00ba7907ac64c3b4d3ef7854663468d755adebc1fbe6e55d9`
-	Entrypoint: `["\/usr\/local\/bin\/dumb-init","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Tue, 05 May 2020 21:20:06 GMT
ADD file:38e2d2a1a0cd8694bd5086f257fdf7504f0c2481bf4f746c9bd1c8d9f3f6430d in / 
# Tue, 05 May 2020 21:20:06 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20200504 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-05-04 00:00:00+01:00
# Tue, 05 May 2020 21:20:07 GMT
CMD ["/bin/bash"]
# Thu, 28 May 2020 17:39:38 GMT
EXPOSE 5601
# Thu, 28 May 2020 17:40:09 GMT
RUN yum update -y && yum install -y fontconfig freetype shadow-utils && yum clean all
# Thu, 28 May 2020 17:40:11 GMT
RUN curl -L -o /usr/local/bin/dumb-init https://github.com/Yelp/dumb-init/releases/download/v1.2.2/dumb-init_1.2.2_amd64
# Thu, 28 May 2020 17:40:11 GMT
RUN echo "37f2c1f0372a45554f1b89924fbb134fc24c3756efaedf11e07f599494e0eff9  /usr/local/bin/dumb-init" | sha256sum -c -
# Thu, 28 May 2020 17:40:12 GMT
RUN chmod +x /usr/local/bin/dumb-init
# Thu, 28 May 2020 17:41:29 GMT
COPY --chown=1000:0dir:0a723e100c1ace947de4b8580f9165767fa682bffb25dec0030b682099a15483 in /usr/share/kibana 
# Thu, 28 May 2020 17:41:31 GMT
WORKDIR /usr/share/kibana
# Thu, 28 May 2020 17:41:33 GMT
RUN ln -s /usr/share/kibana /opt/kibana
# Thu, 28 May 2020 17:41:33 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 28 May 2020 17:41:33 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 May 2020 17:41:33 GMT
COPY --chown=1000:0file:ea1f294356f14dfc1a50e3303613e69f187589962058569d5b3282460d7f28cb in /usr/share/kibana/config/kibana.yml 
# Thu, 28 May 2020 17:41:33 GMT
COPY --chown=1000:0file:8b9c2df36b5315bd3ada649a3e73f7f4011b1df2137c375bb98daad4b6b913c3 in /usr/local/bin/ 
# Thu, 28 May 2020 17:41:35 GMT
RUN chmod g+ws /usr/share/kibana && find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \;
# Thu, 28 May 2020 17:41:37 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} +
# Thu, 28 May 2020 17:41:39 GMT
RUN groupadd --gid 1000 kibana && useradd --uid 1000 --gid 1000 --home-dir /usr/share/kibana --no-create-home kibana
# Thu, 28 May 2020 17:41:39 GMT
USER kibana
# Thu, 28 May 2020 17:41:39 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.label-schema.name=kibana org.label-schema.version=7.7.1 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.license=Elastic License org.label-schema.usage=https://www.elastic.co/guide/en/kibana/index.html org.label-schema.build-date=2020-05-28T17:35:57.341Z license=Elastic License
# Thu, 28 May 2020 17:41:39 GMT
ENTRYPOINT ["/usr/local/bin/dumb-init" "--"]
# Thu, 28 May 2020 17:41:40 GMT
CMD ["/usr/local/bin/kibana-docker"]
```

-	Layers:
	-	`sha256:524b0c1e57f8ee5fee01a1decba2f301c324a6513ca3551021264e3aa7341ebc`  
		Last Modified: Tue, 05 May 2020 21:23:14 GMT  
		Size: 75.9 MB (75880141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:103dc10f20b69176a308ca3df69200ea4728723f058405b47dc420761e1686c2`  
		Last Modified: Wed, 03 Jun 2020 14:42:19 GMT  
		Size: 26.7 MB (26692147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e397e023efd5569838f030d0ab2adfd8b0c655c3b34b0bd2bb7fbbc3ccfa4d1e`  
		Last Modified: Wed, 03 Jun 2020 14:42:13 GMT  
		Size: 31.7 KB (31679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0ee6620405ce41165a5295ed891530a8c81d784d6ae92fa86779ab4d8999d48`  
		Last Modified: Wed, 03 Jun 2020 14:42:13 GMT  
		Size: 30.2 KB (30193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17e4e03944f0d29bc67f1706dc306ee6fb57baf4b909a3f42d1407a69fd1d337`  
		Last Modified: Wed, 03 Jun 2020 14:45:20 GMT  
		Size: 282.0 MB (282011041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eff8f4cc37491e86600580fe11e087dee60a1adaa4b98cea99b39d2529a67c34`  
		Last Modified: Wed, 03 Jun 2020 14:44:30 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa92cc28ed7e2b366a785416be5da1ae75625f7ac8cbdb928d43fa6af0540b2b`  
		Last Modified: Wed, 03 Jun 2020 14:44:30 GMT  
		Size: 387.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afda7e77e6ed80d3cf076120781cabc9806d99a30d40862b8b0288a055f9353d`  
		Last Modified: Wed, 03 Jun 2020 14:44:30 GMT  
		Size: 2.9 KB (2923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:019e109bb7c5eb596a836b269a84f38ff5546890af30d594134450769c74372f`  
		Last Modified: Wed, 03 Jun 2020 14:44:31 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e82949888e472c7ff5925239832f3d4c5f03e74545bae2b5776c1a591e55e9bd`  
		Last Modified: Wed, 03 Jun 2020 14:42:11 GMT  
		Size: 200.6 KB (200613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15f31b4d9a520831acb58d70c1eb80c8099b6ea30c564614ecbf7dd97fddcd52`  
		Last Modified: Wed, 03 Jun 2020 14:44:30 GMT  
		Size: 1.8 KB (1814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

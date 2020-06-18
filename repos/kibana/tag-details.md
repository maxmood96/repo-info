<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `kibana`

-	[`kibana:6.8.10`](#kibana6810)
-	[`kibana:7.8.0`](#kibana780)

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

## `kibana:7.8.0`

```console
$ docker pull kibana@sha256:326ac27cbc363e515e1b660d3117bbad3c5cd140db358ade251195c094db6fda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kibana:7.8.0` - linux; amd64

```console
$ docker pull kibana@sha256:b621369de38b24eb8edc66d419446accee567e6dc0290f6debb24543ba7fbfac
```

-	Docker Version: 19.03.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **440.1 MB (440090065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df0a0da46dd18969158766dc188988eebd365e9e0150d62679d70812994f5aff`
-	Entrypoint: `["\/usr\/local\/bin\/dumb-init","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Tue, 05 May 2020 21:20:06 GMT
ADD file:38e2d2a1a0cd8694bd5086f257fdf7504f0c2481bf4f746c9bd1c8d9f3f6430d in / 
# Tue, 05 May 2020 21:20:06 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20200504 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-05-04 00:00:00+01:00
# Tue, 05 May 2020 21:20:07 GMT
CMD ["/bin/bash"]
# Sun, 14 Jun 2020 20:43:16 GMT
EXPOSE 5601
# Sun, 14 Jun 2020 20:43:53 GMT
RUN yum update -y && yum install -y fontconfig freetype shadow-utils && yum clean all
# Sun, 14 Jun 2020 20:43:54 GMT
RUN curl -L -o /usr/local/bin/dumb-init https://github.com/Yelp/dumb-init/releases/download/v1.2.2/dumb-init_1.2.2_amd64
# Sun, 14 Jun 2020 20:43:55 GMT
RUN echo "37f2c1f0372a45554f1b89924fbb134fc24c3756efaedf11e07f599494e0eff9  /usr/local/bin/dumb-init" | sha256sum -c -
# Sun, 14 Jun 2020 20:43:56 GMT
RUN chmod +x /usr/local/bin/dumb-init
# Sun, 14 Jun 2020 20:45:02 GMT
COPY --chown=1000:0dir:fb0e25c45aaa1b4c5860eeed7d1aaedb0cd963ca230488a5867eeb867269d8a9 in /usr/share/kibana 
# Sun, 14 Jun 2020 20:45:04 GMT
WORKDIR /usr/share/kibana
# Sun, 14 Jun 2020 20:45:06 GMT
RUN ln -s /usr/share/kibana /opt/kibana
# Sun, 14 Jun 2020 20:45:06 GMT
ENV ELASTIC_CONTAINER=true
# Sun, 14 Jun 2020 20:45:07 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 14 Jun 2020 20:45:07 GMT
COPY --chown=1000:0file:ea1f294356f14dfc1a50e3303613e69f187589962058569d5b3282460d7f28cb in /usr/share/kibana/config/kibana.yml 
# Sun, 14 Jun 2020 20:45:07 GMT
COPY --chown=1000:0file:c74a9241cf30de91e0875eec37b3147e632168d86875a5ab57afab208d2c19ab in /usr/local/bin/ 
# Sun, 14 Jun 2020 20:45:09 GMT
RUN chmod g+ws /usr/share/kibana && find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \;
# Sun, 14 Jun 2020 20:45:11 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} +
# Sun, 14 Jun 2020 20:45:12 GMT
RUN groupadd --gid 1000 kibana && useradd --uid 1000 --gid 1000 --home-dir /usr/share/kibana --no-create-home kibana
# Sun, 14 Jun 2020 20:45:13 GMT
USER kibana
# Sun, 14 Jun 2020 20:45:13 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.label-schema.name=kibana org.label-schema.version=7.8.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.license=Elastic License org.label-schema.usage=https://www.elastic.co/guide/en/kibana/index.html org.label-schema.build-date=2020-06-14T20:39:23.401Z license=Elastic License
# Sun, 14 Jun 2020 20:45:13 GMT
ENTRYPOINT ["/usr/local/bin/dumb-init" "--"]
# Sun, 14 Jun 2020 20:45:13 GMT
CMD ["/usr/local/bin/kibana-docker"]
```

-	Layers:
	-	`sha256:524b0c1e57f8ee5fee01a1decba2f301c324a6513ca3551021264e3aa7341ebc`  
		Last Modified: Tue, 05 May 2020 21:23:14 GMT  
		Size: 75.9 MB (75880141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c3c85c9f549e138543663327e2900a5f6e787e12f2c92097c6917b22096d91f`  
		Last Modified: Thu, 18 Jun 2020 20:27:19 GMT  
		Size: 26.7 MB (26699200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75826be8d25e813d300c58a8b51f0b49266f4856c0dc046336125b899b48db8d`  
		Last Modified: Thu, 18 Jun 2020 20:27:13 GMT  
		Size: 31.7 KB (31678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4951867bd56c44907f423b4f5be4d2b9529d08be8377fb8b4d4054f8675abc2`  
		Last Modified: Thu, 18 Jun 2020 20:27:14 GMT  
		Size: 30.2 KB (30194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0af11a7b96b537589df53bc538e1babb70b893216e8669bd607f8b672e2b408`  
		Last Modified: Thu, 18 Jun 2020 20:28:12 GMT  
		Size: 337.2 MB (337242769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f81b8aaeaf3557b3bee0867ebfea1753b851c0cac59951237bac46c5471e708`  
		Last Modified: Thu, 18 Jun 2020 20:27:13 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c52e407927e3cf2beba5ecad3e97787d5bc3c8117f7b8d0d367e22e5324cb0e`  
		Last Modified: Thu, 18 Jun 2020 20:27:12 GMT  
		Size: 387.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ca195712ee98779deda6e8125611455f1f7f116903f87e642d60d66515a6eff`  
		Last Modified: Thu, 18 Jun 2020 20:27:11 GMT  
		Size: 3.0 KB (2990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94650bdbb5bf6d786629173fc50d822a7ac7a1ec3b1729f6c4197abc8772949d`  
		Last Modified: Thu, 18 Jun 2020 20:27:12 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c978c1a82f001a60f021bcdfcc698cd772d652e77a09b78583505b0b4671377e`  
		Last Modified: Thu, 18 Jun 2020 20:27:12 GMT  
		Size: 200.6 KB (200610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50fe1f68e816c492a08660c8d99c90b0c7a8f61ff1b51676889e4be9157439b5`  
		Last Modified: Thu, 18 Jun 2020 20:27:12 GMT  
		Size: 1.8 KB (1815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

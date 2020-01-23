<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `kibana`

-	[`kibana:6.8.6`](#kibana686)
-	[`kibana:7.5.2`](#kibana752)

## `kibana:6.8.6`

```console
$ docker pull kibana@sha256:f773d11d6a4304d1795d63b6877cf7e21bbcb4703d57444325f0a906163a408c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kibana:6.8.6` - linux; amd64

```console
$ docker pull kibana@sha256:0a831b9e3251e777615aed743ba46ebd2b0253cd6e39c7636246515710f78379
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.9 MB (298870006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adfab5632ef4cb6f1458f27dc9e580bb4c6ff04f3d219c9ddb7c92c77e312ea8`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Tue, 12 Nov 2019 00:20:33 GMT
ADD file:45a381049c52b5664e5e911dead277b25fadbae689c0bb35be3c42dff0f2dffe in / 
# Tue, 12 Nov 2019 00:20:33 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20191001
# Tue, 12 Nov 2019 00:20:33 GMT
CMD ["/bin/bash"]
# Fri, 13 Dec 2019 17:58:37 GMT
EXPOSE 5601
# Fri, 13 Dec 2019 17:59:22 GMT
RUN yum update -y && yum install -y fontconfig freetype && yum clean all
# Fri, 13 Dec 2019 18:00:09 GMT
COPY --chown=1000:0dir:b7add46674939973162bad0e77bc7e684546e7577015c708dc2a8dad71ebd2f1 in /usr/share/kibana 
# Fri, 13 Dec 2019 18:00:10 GMT
WORKDIR /usr/share/kibana
# Fri, 13 Dec 2019 18:00:13 GMT
RUN ln -s /usr/share/kibana /opt/kibana
# Fri, 13 Dec 2019 18:00:13 GMT
ENV ELASTIC_CONTAINER=true
# Fri, 13 Dec 2019 18:00:14 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Dec 2019 18:00:16 GMT
COPY --chown=1000:0file:60b6181f28c99b362092ea6139b6d4112ddd0bef32d52563c33b26bdc2b51318 in /usr/share/kibana/config/kibana.yml 
# Fri, 13 Dec 2019 18:00:17 GMT
COPY --chown=1000:0file:af2bc419b515a5fca0bc857249c43a0e082e6cb60c394519993854e4bc8048ca in /usr/local/bin/ 
# Fri, 13 Dec 2019 18:00:20 GMT
RUN chmod g+ws /usr/share/kibana && find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \;
# Fri, 13 Dec 2019 18:00:23 GMT
RUN groupadd --gid 1000 kibana && useradd --uid 1000 --gid 1000 --home-dir /usr/share/kibana --no-create-home kibana
# Fri, 13 Dec 2019 18:00:23 GMT
USER kibana
# Fri, 13 Dec 2019 18:00:24 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.label-schema.name=kibana org.label-schema.version=6.8.6 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.license=Elastic License license=Elastic License
# Fri, 13 Dec 2019 18:00:25 GMT
CMD ["/usr/local/bin/kibana-docker"]
```

-	Layers:
	-	`sha256:ab5ef0e5819490abe86106fd9f4381123e37a03e80e650be39f7938d30ecb530`  
		Last Modified: Tue, 12 Nov 2019 00:23:38 GMT  
		Size: 75.8 MB (75780712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40057de213d2c47a5d196cba4b2e8911f7caba1e0e40ddc45ff5ff1fcda7f560`  
		Last Modified: Wed, 18 Dec 2019 22:13:01 GMT  
		Size: 33.1 MB (33136094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:434b62b0636c274e666fc1bc6c3577a35b48747a0bb19f61a3237bce06a61ada`  
		Last Modified: Wed, 18 Dec 2019 22:13:17 GMT  
		Size: 189.9 MB (189948389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7370972a467b446b5ca4da1b7148e5002914f5c9a4fe4e8d1a5c1cc6c3ecbcd3`  
		Last Modified: Wed, 18 Dec 2019 22:12:49 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e1767103506c625b66853d42b82fe0998a8db43557a61d2ed7ad5bfaedfaac4`  
		Last Modified: Wed, 18 Dec 2019 22:12:49 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83c66d66f9304e3a4ccfd6b61323890268da91f9253179406f2b3ece8f4c4f73`  
		Last Modified: Wed, 18 Dec 2019 22:12:49 GMT  
		Size: 2.3 KB (2259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:590781aeb7f42c4f7573d916a9448a8f3acb4133bf8452c914c7c89cfed95a3f`  
		Last Modified: Wed, 18 Dec 2019 22:12:49 GMT  
		Size: 165.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1efa205edea3066282cf9cd02991379b868214fce810c0260cf0fda78968056`  
		Last Modified: Wed, 18 Dec 2019 22:12:49 GMT  
		Size: 1.8 KB (1847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kibana:7.5.2`

```console
$ docker pull kibana@sha256:70de7dc2df7d70d8d1eed0a13df6db9a3ccc7bba99eea7b20f13825e82e9af08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kibana:7.5.2` - linux; amd64

```console
$ docker pull kibana@sha256:766a860398b484642d6208bb60fd599042c3bbae4622a253bdc45fb2f339652a
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.0 MB (349970876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6e894c36481fa0e539e61f2f847cf561691c4fb0a5c64c31b01d6885dfbd60d`
-	Entrypoint: `["\/usr\/local\/bin\/dumb-init","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Tue, 12 Nov 2019 00:20:33 GMT
ADD file:45a381049c52b5664e5e911dead277b25fadbae689c0bb35be3c42dff0f2dffe in / 
# Tue, 12 Nov 2019 00:20:33 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20191001
# Tue, 12 Nov 2019 00:20:33 GMT
CMD ["/bin/bash"]
# Wed, 15 Jan 2020 13:02:56 GMT
EXPOSE 5601
# Wed, 15 Jan 2020 13:03:30 GMT
RUN yum update -y && yum install -y fontconfig freetype && yum clean all
# Wed, 15 Jan 2020 13:03:32 GMT
RUN curl -L -o /usr/local/bin/dumb-init https://github.com/Yelp/dumb-init/releases/download/v1.2.2/dumb-init_1.2.2_amd64
# Wed, 15 Jan 2020 13:03:33 GMT
RUN echo "37f2c1f0372a45554f1b89924fbb134fc24c3756efaedf11e07f599494e0eff9  /usr/local/bin/dumb-init" | sha256sum -c -
# Wed, 15 Jan 2020 13:03:35 GMT
RUN chmod +x /usr/local/bin/dumb-init
# Wed, 15 Jan 2020 13:04:18 GMT
COPY --chown=1000:0dir:af94206cf05b470534391000d840d1075fc1e365afb5d400284216d9ff294ba0 in /usr/share/kibana 
# Wed, 15 Jan 2020 13:04:22 GMT
WORKDIR /usr/share/kibana
# Wed, 15 Jan 2020 13:04:23 GMT
RUN ln -s /usr/share/kibana /opt/kibana
# Wed, 15 Jan 2020 13:04:23 GMT
ENV ELASTIC_CONTAINER=true
# Wed, 15 Jan 2020 13:04:23 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Jan 2020 13:04:24 GMT
COPY --chown=1000:0file:60b6181f28c99b362092ea6139b6d4112ddd0bef32d52563c33b26bdc2b51318 in /usr/share/kibana/config/kibana.yml 
# Wed, 15 Jan 2020 13:04:24 GMT
COPY --chown=1000:0file:23744f376b12c9d0c1869af33cd3a85883d7c67dfa3f00a276258846b6089898 in /usr/local/bin/ 
# Wed, 15 Jan 2020 13:04:25 GMT
RUN chmod g+ws /usr/share/kibana && find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \;
# Wed, 15 Jan 2020 13:04:26 GMT
RUN groupadd --gid 1000 kibana && useradd --uid 1000 --gid 1000 --home-dir /usr/share/kibana --no-create-home kibana
# Wed, 15 Jan 2020 13:04:26 GMT
USER kibana
# Wed, 15 Jan 2020 13:04:26 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.label-schema.name=kibana org.label-schema.version=7.5.2 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.license=Elastic License license=Elastic License
# Wed, 15 Jan 2020 13:04:26 GMT
ENTRYPOINT ["/usr/local/bin/dumb-init" "--"]
# Wed, 15 Jan 2020 13:04:27 GMT
CMD ["/usr/local/bin/kibana-docker"]
```

-	Layers:
	-	`sha256:ab5ef0e5819490abe86106fd9f4381123e37a03e80e650be39f7938d30ecb530`  
		Last Modified: Tue, 12 Nov 2019 00:23:38 GMT  
		Size: 75.8 MB (75780712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdffd95b4709d5200b2ddd4f15f34777f974d217b2cd8ba6bec1ea62f64eb14a`  
		Last Modified: Tue, 21 Jan 2020 21:31:47 GMT  
		Size: 33.1 MB (33131445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ebee118d38079a7df6efd5eecd6613aba2cdb9d8492873c8d4be0d3b95a0722`  
		Last Modified: Tue, 21 Jan 2020 21:31:34 GMT  
		Size: 31.7 KB (31697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24681010bbc5c051593e8c26524a1df1346dd7cea60125a84a47e3ce3800f35b`  
		Last Modified: Tue, 21 Jan 2020 21:31:34 GMT  
		Size: 30.2 KB (30202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e27591e448a1748d10a505196a0dc048e66e5885632aae63f1b5611992b67d2`  
		Last Modified: Tue, 21 Jan 2020 22:32:49 GMT  
		Size: 241.0 MB (240991761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:056862b48dedebd0e6f8b7ff46c2d665992a5c30def9aedce17d2b9e95bdd255`  
		Last Modified: Tue, 21 Jan 2020 22:32:11 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a273b62cf9d96f121efa81e210a0fe32618ede18d27c9106d66de4d34e3b9470`  
		Last Modified: Tue, 21 Jan 2020 22:32:11 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72a7d32da5588f30c8e4d066ab13cb984132459c3e0407fe7d712b34771748ca`  
		Last Modified: Tue, 21 Jan 2020 22:32:11 GMT  
		Size: 2.5 KB (2501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9384e8664edc614c1cfc42c0d5111795edf5b75d73fd461cfec054e057454430`  
		Last Modified: Tue, 21 Jan 2020 22:32:11 GMT  
		Size: 166.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:697b6c2d2d8ade51abf99213787f5ce86938c914a3128e26c053e94c41b9245a`  
		Last Modified: Tue, 21 Jan 2020 22:32:11 GMT  
		Size: 1.8 KB (1848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

# `maven:3.9.8-amazoncorretto-11-al2023`

## Docker Metadata

- Image ID: `sha256:cf25ca2c4e6c6c5ab362e4d59c617477434461694c0d61761dbe2d70636b6cf5`
- Created: `2024-06-27T09:17:07Z`
- Virtual Size: ~ 522.54 Mb  
  (total size of all layers on-disk)
- Arch: `linux`/`amd64`
- Entrypoint: `["/usr/local/bin/mvn-entrypoint.sh"]`
- Command: `["mvn"]`
- Environment:
  - `PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin`
  - `LANG=C.UTF-8`
  - `JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto`
  - `MAVEN_HOME=/usr/share/maven`
  - `MAVEN_CONFIG=/root/.m2`
- Labels:
  - `org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.`
  - `org.opencontainers.image.source=https://github.com/carlossg/docker-maven`
  - `org.opencontainers.image.title=Apache Maven`
  - `org.opencontainers.image.url=https://github.com/carlossg/docker-maven`

## `rpm` (`.rpm`-based packages)

### `rpm` package: `alsa-lib-1.2.7.2-1.amzn2023.0.2.x86_64`

Licenses (from `rpm --query`): LGPLv2+

Source:

```console
$ dnf --quiet download --source --url alsa-lib-1.2.7.2-1.amzn2023.0.2
https://cdn.amazonlinux.com/al2023/core/guids/78a1f37d281a9c8eb5115c4f9b2f8306b103426d1c252c1a59e532225ea7a73b/SRPMS/../../../../blobstore/417a8cce6b248f51be00a4ea85839d87b3ed38535b81d1fe4a8696eea3266e78/alsa-lib-1.2.7.2-1.amzn2023.0.2.src.rpm
```

### `rpm` package: `alternatives-1.15-2.amzn2023.0.2.x86_64`

Licenses (from `rpm --query`): GPLv2

Source:

```console
$ dnf --quiet download --source --url alternatives-1.15-2.amzn2023.0.2
https://cdn.amazonlinux.com/al2023/core/guids/78a1f37d281a9c8eb5115c4f9b2f8306b103426d1c252c1a59e532225ea7a73b/SRPMS/../../../../blobstore/4294b160d9f7169d1393a9e5b061b6c6eb5ab5c181ab7137998b8bcaff9102e3/chkconfig-1.15-2.amzn2023.0.2.src.rpm
```

### `rpm` package: `amazon-linux-repo-cdn-2023.5.20240708-1.amzn2023.noarch`

Licenses (from `rpm --query`): MIT

Source:

```console
$ dnf --quiet download --source --url amazon-linux-repo-cdn-2023.5.20240708-1.amzn2023.noarch
https://cdn.amazonlinux.com/al2023/core/guids/78a1f37d281a9c8eb5115c4f9b2f8306b103426d1c252c1a59e532225ea7a73b/SRPMS/../../../../blobstore/61553bd93aa64dc68f6cac839342047d90b93541f26966889cbd8fb13ce9bb26/system-release-2023.5.20240708-1.amzn2023.src.rpm
```

### `rpm` package: `audit-libs-3.0.6-1.amzn2023.0.2.x86_64`

Licenses (from `rpm --query`): LGPLv2+

Source:

```console
$ dnf --quiet download --source --url audit-libs-3.0.6-1.amzn2023.0.2
https://cdn.amazonlinux.com/al2023/core/guids/78a1f37d281a9c8eb5115c4f9b2f8306b103426d1c252c1a59e532225ea7a73b/SRPMS/../../../../blobstore/59bb12b70c73c3c6f68e85153b0bad794b325e1226a439efb81e7452b491c915/audit-3.0.6-1.amzn2023.0.2.src.rpm
```

### `rpm` package: `basesystem-11-11.amzn2023.0.2.noarch`

Licenses (from `rpm --query`): Public Domain

Source:

```console
$ dnf --quiet download --source --url basesystem-11-11.amzn2023.0.2.noarch
https://cdn.amazonlinux.com/al2023/core/guids/78a1f37d281a9c8eb5115c4f9b2f8306b103426d1c252c1a59e532225ea7a73b/SRPMS/../../../../blobstore/25e3bc7c2b357da6a91f5c94215030cd00bc9fd28e3c76f9581ad7ca1ba2d61d/basesystem-11-11.amzn2023.0.2.src.rpm
```

### `rpm` package: `bash-5.2.15-1.amzn2023.0.2.x86_64`

Licenses (from `rpm --query`): GPLv3+

Source:

```console
$ dnf --quiet download --source --url bash-5.2.15-1.amzn2023.0.2
https://cdn.amazonlinux.com/al2023/core/guids/78a1f37d281a9c8eb5115c4f9b2f8306b103426d1c252c1a59e532225ea7a73b/SRPMS/../../../../blobstore/99c1698d2e23e936a8812c11369bd66362e6e324f4178074a67d8f6c6c991be1/bash-5.2.15-1.amzn2023.0.2.src.rpm
```

### `rpm` package: `bzip2-libs-1.0.8-6.amzn2023.0.2.x86_64`

Licenses (from `rpm --query`): BSD

Source:

```console
$ dnf --quiet download --source --url bzip2-libs-1.0.8-6.amzn2023.0.2
https://cdn.amazonlinux.com/al2023/core/guids/78a1f37d281a9c8eb5115c4f9b2f8306b103426d1c252c1a59e532225ea7a73b/SRPMS/../../../../blobstore/44142b622640d1ec7703982fd963e4886f23fb34f5e4f2ee7dfe9e03af4373a4/bzip2-1.0.8-6.amzn2023.0.2.src.rpm
```

### `rpm` package: `ca-certificates-2023.2.64-1.0.amzn2023.0.1.noarch`

Licenses (from `rpm --query`): Public Domain

Source:

```console
$ dnf --quiet download --source --url ca-certificates-2023.2.64-1.0.amzn2023.0.1.noarch
https://cdn.amazonlinux.com/al2023/core/guids/78a1f37d281a9c8eb5115c4f9b2f8306b103426d1c252c1a59e532225ea7a73b/SRPMS/../../../../blobstore/3f2d425e7f702881d9d57ac8e1a796d70603d361f0c375038bf667051f0e9526/ca-certificates-2023.2.64-1.0.amzn2023.0.1.src.rpm
```

### `rpm` package: `cairo-1.17.6-2.amzn2023.0.1.x86_64`

Licenses (from `rpm --query`): LGPLv2 or MPLv1.1

Source:

```console
$ dnf --quiet download --source --url cairo-1.17.6-2.amzn2023.0.1
https://cdn.amazonlinux.com/al2023/core/guids/78a1f37d281a9c8eb5115c4f9b2f8306b103426d1c252c1a59e532225ea7a73b/SRPMS/../../../../blobstore/edafb8bf720b2ee43d06298e7c5eed3bc272819e7b42bcc6de6ddbe7341ab419/cairo-1.17.6-2.amzn2023.0.1.src.rpm
```

### `rpm` package: `chkconfig-1.15-2.amzn2023.0.2.x86_64`

Licenses (from `rpm --query`): GPLv2

Source:

```console
$ dnf --quiet download --source --url chkconfig-1.15-2.amzn2023.0.2
https://cdn.amazonlinux.com/al2023/core/guids/78a1f37d281a9c8eb5115c4f9b2f8306b103426d1c252c1a59e532225ea7a73b/SRPMS/../../../../blobstore/4294b160d9f7169d1393a9e5b061b6c6eb5ab5c181ab7137998b8bcaff9102e3/chkconfig-1.15-2.amzn2023.0.2.src.rpm
```

### `rpm` package: `coreutils-single-8.32-30.amzn2023.0.3.x86_64`

Licenses (from `rpm --query`): GPLv3+

Source:

```console
$ dnf --quiet download --source --url coreutils-single-8.32-30.amzn2023.0.3
https://cdn.amazonlinux.com/al2023/core/guids/78a1f37d281a9c8eb5115c4f9b2f8306b103426d1c252c1a59e532225ea7a73b/SRPMS/../../../../blobstore/eda7b6481dd3a0dfdcc6e08e315c9a0b4f441ecc8b357cfd5524d999e777760a/coreutils-8.32-30.amzn2023.0.3.src.rpm
```

### `rpm` package: `crypto-policies-20220428-1.gitdfb10ea.amzn2023.0.2.noarch`

Licenses (from `rpm --query`): LGPLv2+

Source:

```console
$ dnf --quiet download --source --url crypto-policies-20220428-1.gitdfb10ea.amzn2023.0.2.noarch
https://cdn.amazonlinux.com/al2023/core/guids/78a1f37d281a9c8eb5115c4f9b2f8306b103426d1c252c1a59e532225ea7a73b/SRPMS/../../../../blobstore/e5cf3be3c197ccf70ab58e68d91d5434cec59c83e03b76cb8793ba0850ccba60/crypto-policies-20220428-1.gitdfb10ea.amzn2023.0.2.src.rpm
```

### `rpm` package: `curl-minimal-8.5.0-1.amzn2023.0.4.x86_64`

Licenses (from `rpm --query`): curl

Source:

```console
$ dnf --quiet download --source --url curl-minimal-8.5.0-1.amzn2023.0.4
https://cdn.amazonlinux.com/al2023/core/guids/78a1f37d281a9c8eb5115c4f9b2f8306b103426d1c252c1a59e532225ea7a73b/SRPMS/../../../../blobstore/06df1530ceda85d884d0fd3ccf87402e9c3b56125f93d8bec8b96cc75f15c5c8/curl-8.5.0-1.amzn2023.0.4.src.rpm
```

### `rpm` package: `dejavu-sans-fonts-2.37-16.amzn2023.0.2.noarch`

Licenses (from `rpm --query`): Bitstream Vera and Public Domain

Source:

```console
$ dnf --quiet download --source --url dejavu-sans-fonts-2.37-16.amzn2023.0.2.noarch
https://cdn.amazonlinux.com/al2023/core/guids/78a1f37d281a9c8eb5115c4f9b2f8306b103426d1c252c1a59e532225ea7a73b/SRPMS/../../../../blobstore/b0c2c83c5393671c135f45902e4d5df5d7535faa1d32382706562fc17ddf320f/dejavu-fonts-2.37-16.amzn2023.0.2.src.rpm
```

### `rpm` package: `dejavu-sans-mono-fonts-2.37-16.amzn2023.0.2.noarch`

Licenses (from `rpm --query`): Bitstream Vera and Public Domain

Source:

```console
$ dnf --quiet download --source --url dejavu-sans-mono-fonts-2.37-16.amzn2023.0.2.noarch
https://cdn.amazonlinux.com/al2023/core/guids/78a1f37d281a9c8eb5115c4f9b2f8306b103426d1c252c1a59e532225ea7a73b/SRPMS/../../../../blobstore/b0c2c83c5393671c135f45902e4d5df5d7535faa1d32382706562fc17ddf320f/dejavu-fonts-2.37-16.amzn2023.0.2.src.rpm
```

### `rpm` package: `dejavu-serif-fonts-2.37-16.amzn2023.0.2.noarch`

Licenses (from `rpm --query`): Bitstream Vera and Public Domain

Source:

```console
$ dnf --quiet download --source --url dejavu-serif-fonts-2.37-16.amzn2023.0.2.noarch
https://cdn.amazonlinux.com/al2023/core/guids/78a1f37d281a9c8eb5115c4f9b2f8306b103426d1c252c1a59e532225ea7a73b/SRPMS/../../../../blobstore/b0c2c83c5393671c135f45902e4d5df5d7535faa1d32382706562fc17ddf320f/dejavu-fonts-2.37-16.amzn2023.0.2.src.rpm
```

### `rpm` package: `dnf-4.14.0-1.amzn2023.0.5.noarch`

Licenses (from `rpm --query`): GPLv2+

Source:

```console
$ dnf --quiet download --source --url dnf-4.14.0-1.amzn2023.0.5.noarch
https://cdn.amazonlinux.com/al2023/core/guids/78a1f37d281a9c8eb5115c4f9b2f8306b103426d1c252c1a59e532225ea7a73b/SRPMS/../../../../blobstore/3c7a286acf75f92e2600171b3b97237f9db9bf5b9466013b3c1686501ad6e7cd/dnf-4.14.0-1.amzn2023.0.5.src.rpm
```

### `rpm` package: `dnf-data-4.14.0-1.amzn2023.0.5.noarch`

Licenses (from `rpm --query`): GPLv2+

Source:

```console
$ dnf --quiet download --source --url dnf-data-4.14.0-1.amzn2023.0.5.noarch
https://cdn.amazonlinux.com/al2023/core/guids/78a1f37d281a9c8eb5115c4f9b2f8306b103426d1c252c1a59e532225ea7a73b/SRPMS/../../../../blobstore/3c7a286acf75f92e2600171b3b97237f9db9bf5b9466013b3c1686501ad6e7cd/dnf-4.14.0-1.amzn2023.0.5.src.rpm
```

### `rpm` package: `elfutils-default-yama-scope-0.188-3.amzn2023.0.2.noarch`

Licenses (from `rpm --query`): GPLv2+ or LGPLv3+

Source:

```console
$ dnf --quiet download --source --url elfutils-default-yama-scope-0.188-3.amzn2023.0.2.noarch
https://cdn.amazonlinux.com/al2023/core/guids/78a1f37d281a9c8eb5115c4f9b2f8306b103426d1c252c1a59e532225ea7a73b/SRPMS/../../../../blobstore/ca54f5b87c67588162356e1347d6d09270fb00325173fbc6a3cbcd4ec349e159/elfutils-0.188-3.amzn2023.0.2.src.rpm
```

### `rpm` package: `elfutils-libelf-0.188-3.amzn2023.0.2.x86_64`

Licenses (from `rpm --query`): GPLv2+ or LGPLv3+

Source:

```console
$ dnf --quiet download --source --url elfutils-libelf-0.188-3.amzn2023.0.2
https://cdn.amazonlinux.com/al2023/core/guids/78a1f37d281a9c8eb5115c4f9b2f8306b103426d1c252c1a59e532225ea7a73b/SRPMS/../../../../blobstore/ca54f5b87c67588162356e1347d6d09270fb00325173fbc6a3cbcd4ec349e159/elfutils-0.188-3.amzn2023.0.2.src.rpm
```

### `rpm` package: `elfutils-libs-0.188-3.amzn2023.0.2.x86_64`

Licenses (from `rpm --query`): GPLv2+ or LGPLv3+

Source:

```console
$ dnf --quiet download --source --url elfutils-libs-0.188-3.amzn2023.0.2
https://cdn.amazonlinux.com/al2023/core/guids/78a1f37d281a9c8eb5115c4f9b2f8306b103426d1c252c1a59e532225ea7a73b/SRPMS/../../../../blobstore/ca54f5b87c67588162356e1347d6d09270fb00325173fbc6a3cbcd4ec349e159/elfutils-0.188-3.amzn2023.0.2.src.rpm
```

### `rpm` package: `expat-2.5.0-1.amzn2023.0.4.x86_64`

Licenses (from `rpm --query`): MIT

Source:

```console
$ dnf --quiet download --source --url expat-2.5.0-1.amzn2023.0.4
https://cdn.amazonlinux.com/al2023/core/guids/78a1f37d281a9c8eb5115c4f9b2f8306b103426d1c252c1a59e532225ea7a73b/SRPMS/../../../../blobstore/49c3a68c3680694d0f30ba9eb3af77fd65d18edd607510b04d74fa728cb24688/expat-2.5.0-1.amzn2023.0.4.src.rpm
```

### `rpm` package: `file-libs-5.39-7.amzn2023.0.4.x86_64`

Licenses (from `rpm --query`): BSD

Source:

```console
$ dnf --quiet download --source --url file-libs-5.39-7.amzn2023.0.4
https://cdn.amazonlinux.com/al2023/core/guids/78a1f37d281a9c8eb5115c4f9b2f8306b103426d1c252c1a59e532225ea7a73b/SRPMS/../../../../blobstore/8428ddd0fc87b93b688c26607c20be3485ca344c65d9b63d4b39bb1ba34d7d6f/file-5.39-7.amzn2023.0.4.src.rpm
```

### `rpm` package: `filesystem-3.14-5.amzn2023.0.3.x86_64`

Licenses (from `rpm --query`): Public Domain

Source:

```console
$ dnf --quiet download --source --url filesystem-3.14-5.amzn2023.0.3
https://cdn.amazonlinux.com/al2023/core/guids/78a1f37d281a9c8eb5115c4f9b2f8306b103426d1c252c1a59e532225ea7a73b/SRPMS/../../../../blobstore/5df3821dcd7b584e67c5e02c6b5c9cff32bee0118e263d7602148432375e398c/filesystem-3.14-5.amzn2023.0.3.src.rpm
```

### `rpm` package: `findutils-4.8.0-2.amzn2023.0.2.x86_64`

Licenses (from `rpm --query`): GPLv3+

Source:

```console
$ dnf --quiet download --source --url findutils-4.8.0-2.amzn2023.0.2
https://cdn.amazonlinux.com/al2023/core/guids/78a1f37d281a9c8eb5115c4f9b2f8306b103426d1c252c1a59e532225ea7a73b/SRPMS/../../../../blobstore/d38118808ee85787845a67279e1fe96530adc794c734ee89942325946a8490fb/findutils-4.8.0-2.amzn2023.0.2.src.rpm
```

### `rpm` package: `fontconfig-2.13.94-2.amzn2023.0.2.x86_64`

Licenses (from `rpm --query`): MIT and Public Domain and UCD

Source:

```console
$ dnf --quiet download --source --url fontconfig-2.13.94-2.amzn2023.0.2
https://cdn.amazonlinux.com/al2023/core/guids/78a1f37d281a9c8eb5115c4f9b2f8306b103426d1c252c1a59e532225ea7a73b/SRPMS/../../../../blobstore/7d1d03c11bd3b705263af6974dcbefd23b8d9668e6d4d1082c42487a73043dff/fontconfig-2.13.94-2.amzn2023.0.2.src.rpm
```

### `rpm` package: `fonts-filesystem-2.0.5-12.amzn2023.0.2.noarch`

Licenses (from `rpm --query`): MIT

Source:

```console
$ dnf --quiet download --source --url fonts-filesystem-2.0.5-12.amzn2023.0.2.noarch
https://cdn.amazonlinux.com/al2023/core/guids/78a1f37d281a9c8eb5115c4f9b2f8306b103426d1c252c1a59e532225ea7a73b/SRPMS/../../../../blobstore/57d60d7f9287825194a2876a6566fd6f5adc5f7bd51e94b3b4fc4fb683f179e4/fonts-rpm-macros-2.0.5-12.amzn2023.0.2.src.rpm
```

### `rpm` package: `freetype-2.13.0-2.amzn2023.0.1.x86_64`

Licenses (from `rpm --query`): (FTL or GPLv2+) and BSD and MIT and Public Domain and zlib with acknowledgement

Source:

```console
$ dnf --quiet download --source --url freetype-2.13.0-2.amzn2023.0.1
https://cdn.amazonlinux.com/al2023/core/guids/78a1f37d281a9c8eb5115c4f9b2f8306b103426d1c252c1a59e532225ea7a73b/SRPMS/../../../../blobstore/51c900bf0366555967b4e6901d41478fdf0b88183d421add1ade7ddb2583ee9f/freetype-2.13.0-2.amzn2023.0.1.src.rpm
```

### `rpm` package: `gawk-5.1.0-3.amzn2023.0.3.x86_64`

Licenses (from `rpm --query`): GPLv3+ and GPLv2+ and LGPLv2+ and BSD

Source:

```console
$ dnf --quiet download --source --url gawk-5.1.0-3.amzn2023.0.3
https://cdn.amazonlinux.com/al2023/core/guids/78a1f37d281a9c8eb5115c4f9b2f8306b103426d1c252c1a59e532225ea7a73b/SRPMS/../../../../blobstore/212e39b4609e36d3f8d02316ad4f9909a28d90e1e9c412174347ad0a78905d84/gawk-5.1.0-3.amzn2023.0.3.src.rpm
```

### `rpm` package: `gdbm-libs-1.19-2.amzn2023.0.2.x86_64`

Licenses (from `rpm --query`): GPLv3+

Source:

```console
$ dnf --quiet download --source --url gdbm-libs-1.19-2.amzn2023.0.2
https://cdn.amazonlinux.com/al2023/core/guids/78a1f37d281a9c8eb5115c4f9b2f8306b103426d1c252c1a59e532225ea7a73b/SRPMS/../../../../blobstore/7289cdd6f7a54c962de48a332d2b471deb0ec6e3aa1fa98c21c9f9ba12870417/gdbm-1.19-2.amzn2023.0.2.src.rpm
```

### `rpm` package: `giflib-5.2.1-9.amzn2023.0.1.x86_64`

Licenses (from `rpm --query`): MIT

Source:

```console
$ dnf --quiet download --source --url giflib-5.2.1-9.amzn2023.0.1
https://cdn.amazonlinux.com/al2023/core/guids/78a1f37d281a9c8eb5115c4f9b2f8306b103426d1c252c1a59e532225ea7a73b/SRPMS/../../../../blobstore/7d8459b6347cf25060ba754d91dd82cb1182534fdaf0d5f6b7155d3a96eb7554/giflib-5.2.1-9.amzn2023.0.1.src.rpm
```

### `rpm` package: `glib2-2.74.7-689.amzn2023.0.2.x86_64`

Licenses (from `rpm --query`): LGPLv2+

Source:

```console
$ dnf --quiet download --source --url glib2-2.74.7-689.amzn2023.0.2
https://cdn.amazonlinux.com/al2023/core/guids/78a1f37d281a9c8eb5115c4f9b2f8306b103426d1c252c1a59e532225ea7a73b/SRPMS/../../../../blobstore/d6e2ef718994d4ea70b5d5cb5068b4efb98c7b0e3a31b72a7a7e74fa7dc74ab8/glib2-2.74.7-689.amzn2023.0.2.src.rpm
```

### `rpm` package: `glibc-2.34-52.amzn2023.0.10.x86_64`

Licenses (from `rpm --query`): LGPLv2+ and LGPLv2+ with exceptions and GPLv2+ and GPLv2+ with exceptions and BSD and Inner-Net and ISC and Public Domain and GFDL

Source:

```console
$ dnf --quiet download --source --url glibc-2.34-52.amzn2023.0.10
https://cdn.amazonlinux.com/al2023/core/guids/78a1f37d281a9c8eb5115c4f9b2f8306b103426d1c252c1a59e532225ea7a73b/SRPMS/../../../../blobstore/cdeb5a179603b6275f2bc2dbaa9471fa0c194b6a5b8471de436e61ee0d1ed202/glibc-2.34-52.amzn2023.0.10.src.rpm
```

### `rpm` package: `glibc-common-2.34-52.amzn2023.0.10.x86_64`

Licenses (from `rpm --query`): LGPLv2+ and LGPLv2+ with exceptions and GPLv2+ and GPLv2+ with exceptions and BSD and Inner-Net and ISC and Public Domain and GFDL

Source:

```console
$ dnf --quiet download --source --url glibc-common-2.34-52.amzn2023.0.10
https://cdn.amazonlinux.com/al2023/core/guids/78a1f37d281a9c8eb5115c4f9b2f8306b103426d1c252c1a59e532225ea7a73b/SRPMS/../../../../blobstore/cdeb5a179603b6275f2bc2dbaa9471fa0c194b6a5b8471de436e61ee0d1ed202/glibc-2.34-52.amzn2023.0.10.src.rpm
```

### `rpm` package: `glibc-minimal-langpack-2.34-52.amzn2023.0.10.x86_64`

Licenses (from `rpm --query`): LGPLv2+ and LGPLv2+ with exceptions and GPLv2+ and GPLv2+ with exceptions and BSD and Inner-Net and ISC and Public Domain and GFDL

Source:

```console
$ dnf --quiet download --source --url glibc-minimal-langpack-2.34-52.amzn2023.0.10
https://cdn.amazonlinux.com/al2023/core/guids/78a1f37d281a9c8eb5115c4f9b2f8306b103426d1c252c1a59e532225ea7a73b/SRPMS/../../../../blobstore/cdeb5a179603b6275f2bc2dbaa9471fa0c194b6a5b8471de436e61ee0d1ed202/glibc-2.34-52.amzn2023.0.10.src.rpm
```

### `rpm` package: `gmp-6.2.1-2.amzn2023.0.2.x86_64`

Licenses (from `rpm --query`): LGPLv3+ or GPLv2+

Source:

```console
$ dnf --quiet download --source --url gmp-6.2.1-2.amzn2023.0.2
https://cdn.amazonlinux.com/al2023/core/guids/78a1f37d281a9c8eb5115c4f9b2f8306b103426d1c252c1a59e532225ea7a73b/SRPMS/../../../../blobstore/ce41b2079bcd3a2bf9e4cb590b8731a8113ba0929aece4dabbd48d7382dc8699/gmp-6.2.1-2.amzn2023.0.2.src.rpm
```

### `rpm` package: `gnupg2-minimal-2.3.7-1.amzn2023.0.4.x86_64`

Licenses (from `rpm --query`): GPLv3+

Source:

```console
$ dnf --quiet download --source --url gnupg2-minimal-2.3.7-1.amzn2023.0.4
https://cdn.amazonlinux.com/al2023/core/guids/78a1f37d281a9c8eb5115c4f9b2f8306b103426d1c252c1a59e532225ea7a73b/SRPMS/../../../../blobstore/a8dc239acd5318dfc1b07235a50696dc781fedba36180d0c7d88951eb9960dc8/gnupg2-2.3.7-1.amzn2023.0.4.src.rpm
```

### `rpm` package: `google-noto-fonts-common-20201206-2.amzn2023.0.2.noarch`

Licenses (from `rpm --query`): OFL

Source:

```console
$ dnf --quiet download --source --url google-noto-fonts-common-20201206-2.amzn2023.0.2.noarch
https://cdn.amazonlinux.com/al2023/core/guids/78a1f37d281a9c8eb5115c4f9b2f8306b103426d1c252c1a59e532225ea7a73b/SRPMS/../../../../blobstore/324137a2353484a66e55cfc1b89645b371175166a3692936d0047bcfef44a77f/google-noto-fonts-20201206-2.amzn2023.0.2.src.rpm
```

### `rpm` package: `google-noto-sans-vf-fonts-20201206-2.amzn2023.0.2.noarch`

Licenses (from `rpm --query`): OFL

Source:

```console
$ dnf --quiet download --source --url google-noto-sans-vf-fonts-20201206-2.amzn2023.0.2.noarch
https://cdn.amazonlinux.com/al2023/core/guids/78a1f37d281a9c8eb5115c4f9b2f8306b103426d1c252c1a59e532225ea7a73b/SRPMS/../../../../blobstore/324137a2353484a66e55cfc1b89645b371175166a3692936d0047bcfef44a77f/google-noto-fonts-20201206-2.amzn2023.0.2.src.rpm
```

### `rpm` package: `gpg-pubkey-d832c631-6515c85e`

Licenses (from `rpm --query`): pubkey

**WARNING:** unable to find source (`dnf download` failed or returned no results)!

### `rpm` package: `gpgme-1.15.1-6.amzn2023.0.3.x86_64`

Licenses (from `rpm --query`): LGPLv2+

Source:

```console
$ dnf --quiet download --source --url gpgme-1.15.1-6.amzn2023.0.3
https://cdn.amazonlinux.com/al2023/core/guids/78a1f37d281a9c8eb5115c4f9b2f8306b103426d1c252c1a59e532225ea7a73b/SRPMS/../../../../blobstore/99fedbc2cb2281dee4a51cbf47ec00c853e5f3e345135cd3c7a6a9424a9eb316/gpgme-1.15.1-6.amzn2023.0.3.src.rpm
```

### `rpm` package: `graphite2-1.3.14-7.amzn2023.0.2.x86_64`

Licenses (from `rpm --query`): (LGPLv2+ or GPLv2+ or MPLv1.1) and (Netscape or GPLv2+ or LGPLv2+)

Source:

```console
$ dnf --quiet download --source --url graphite2-1.3.14-7.amzn2023.0.2
https://cdn.amazonlinux.com/al2023/core/guids/78a1f37d281a9c8eb5115c4f9b2f8306b103426d1c252c1a59e532225ea7a73b/SRPMS/../../../../blobstore/e55aaabc288dec64da7e43fec2f85e72842a20b0c762e328cbcfe9c33f979d77/graphite2-1.3.14-7.amzn2023.0.2.src.rpm
```

### `rpm` package: `grep-3.8-1.amzn2023.0.4.x86_64`

Licenses (from `rpm --query`): GPLv3+

Source:

```console
$ dnf --quiet download --source --url grep-3.8-1.amzn2023.0.4
https://cdn.amazonlinux.com/al2023/core/guids/78a1f37d281a9c8eb5115c4f9b2f8306b103426d1c252c1a59e532225ea7a73b/SRPMS/../../../../blobstore/2ffdc0cda5bb0d20b5a87a2868d8bea572fbe257030be915a49d2e439d8cd459/grep-3.8-1.amzn2023.0.4.src.rpm
```

### `rpm` package: `gzip-1.12-1.amzn2023.0.1.x86_64`

Licenses (from `rpm --query`): GPLv3+ and GFDL

Source:

```console
$ dnf --quiet download --source --url gzip-1.12-1.amzn2023.0.1
https://cdn.amazonlinux.com/al2023/core/guids/78a1f37d281a9c8eb5115c4f9b2f8306b103426d1c252c1a59e532225ea7a73b/SRPMS/../../../../blobstore/1efab64447a2051db3c054ca4d367135a6f6861ba7d2f16353ceba0bfcbfd94e/gzip-1.12-1.amzn2023.0.1.src.rpm
```

### `rpm` package: `harfbuzz-7.0.0-2.amzn2023.0.1.x86_64`

Licenses (from `rpm --query`): MIT

Source:

```console
$ dnf --quiet download --source --url harfbuzz-7.0.0-2.amzn2023.0.1
https://cdn.amazonlinux.com/al2023/core/guids/78a1f37d281a9c8eb5115c4f9b2f8306b103426d1c252c1a59e532225ea7a73b/SRPMS/../../../../blobstore/d70feb6e7549ac8924e67a88f2fbdf3020857ac13bf8c72e9c5ac6161381f302/harfbuzz-7.0.0-2.amzn2023.0.1.src.rpm
```

### `rpm` package: `java-11-amazon-corretto-11.0.24+8-1.amzn2023.x86_64`

Licenses (from `rpm --query`): ASL 1.1 and ASL 2.0 and BSD and BSD with advertising and GPL+ and GPLv2 and GPLv2 with exceptions and IJG and LGPLv2+ and MIT and MPLv2.0 and Public Domain and W3C and zlib and ISC and FTL and RSA.

**WARNING:** unable to find source (`dnf download` failed or returned no results)!

### `rpm` package: `java-11-amazon-corretto-devel-11.0.24+8-1.amzn2023.x86_64`

Licenses (from `rpm --query`): ASL 1.1 and ASL 2.0 and BSD and BSD with advertising and GPL+ and GPLv2 and GPLv2 with exceptions and IJG and LGPLv2+ and MIT and MPLv2.0 and Public Domain and W3C and zlib and ISC and FTL and RSA.

**WARNING:** unable to find source (`dnf download` failed or returned no results)!

### `rpm` package: `java-11-amazon-corretto-headless-11.0.24+8-1.amzn2023.x86_64`

Licenses (from `rpm --query`): ASL 1.1 and ASL 2.0 and BSD and BSD with advertising and GPL+ and GPLv2 and GPLv2 with exceptions and IJG and LGPLv2+ and MIT and MPLv2.0 and Public Domain and W3C and zlib and ISC and FTL and RSA.

**WARNING:** unable to find source (`dnf download` failed or returned no results)!

### `rpm` package: `java-11-amazon-corretto-jmods-11.0.24+8-1.amzn2023.x86_64`

Licenses (from `rpm --query`): ASL 1.1 and ASL 2.0 and BSD and BSD with advertising and GPL+ and GPLv2 and GPLv2 with exceptions and IJG and LGPLv2+ and MIT and MPLv2.0 and Public Domain and W3C and zlib and ISC and FTL and RSA.

**WARNING:** unable to find source (`dnf download` failed or returned no results)!

### `rpm` package: `javapackages-filesystem-6.0.0-7.amzn2023.0.6.noarch`

Licenses (from `rpm --query`): BSD

Source:

```console
$ dnf --quiet download --source --url javapackages-filesystem-6.0.0-7.amzn2023.0.6.noarch
https://cdn.amazonlinux.com/al2023/core/guids/78a1f37d281a9c8eb5115c4f9b2f8306b103426d1c252c1a59e532225ea7a73b/SRPMS/../../../../blobstore/823d556d9261802eec3c78bfa1b6a48f0aa082813ff037e9cb8c5ca5a8ec21c2/javapackages-tools-6.0.0-7.amzn2023.0.6.src.rpm
```

### `rpm` package: `json-c-0.14-8.amzn2023.0.2.x86_64`

Licenses (from `rpm --query`): MIT

Source:

```console
$ dnf --quiet download --source --url json-c-0.14-8.amzn2023.0.2
https://cdn.amazonlinux.com/al2023/core/guids/78a1f37d281a9c8eb5115c4f9b2f8306b103426d1c252c1a59e532225ea7a73b/SRPMS/../../../../blobstore/11f48e71e93d6c9343029363a134098ac3e72abb12ef4a7e97a312834b3ef5b9/json-c-0.14-8.amzn2023.0.2.src.rpm
```

### `rpm` package: `keyutils-libs-1.6.3-1.amzn2023.0.1.x86_64`

Licenses (from `rpm --query`): GPLv2+ and LGPLv2+

Source:

```console
$ dnf --quiet download --source --url keyutils-libs-1.6.3-1.amzn2023.0.1
https://cdn.amazonlinux.com/al2023/core/guids/78a1f37d281a9c8eb5115c4f9b2f8306b103426d1c252c1a59e532225ea7a73b/SRPMS/../../../../blobstore/05bc74122236af00e08cc34f2b7cb6982951e1b34f243af393283c153862f8e3/keyutils-1.6.3-1.amzn2023.0.1.src.rpm
```

### `rpm` package: `krb5-libs-1.21-3.amzn2023.0.4.x86_64`

Licenses (from `rpm --query`): MIT

Source:

```console
$ dnf --quiet download --source --url krb5-libs-1.21-3.amzn2023.0.4
https://cdn.amazonlinux.com/al2023/core/guids/78a1f37d281a9c8eb5115c4f9b2f8306b103426d1c252c1a59e532225ea7a73b/SRPMS/../../../../blobstore/8d57db1454ff43b52b318a6e8feef395804539d013433c6bb16f23afcd990675/krb5-1.21-3.amzn2023.0.4.src.rpm
```

### `rpm` package: `langpacks-core-font-en-3.0-21.amzn2023.0.4.noarch`

Licenses (from `rpm --query`): GPLv2+

Source:

```console
$ dnf --quiet download --source --url langpacks-core-font-en-3.0-21.amzn2023.0.4.noarch
https://cdn.amazonlinux.com/al2023/core/guids/78a1f37d281a9c8eb5115c4f9b2f8306b103426d1c252c1a59e532225ea7a73b/SRPMS/../../../../blobstore/cf2d1ff906ce456120e2791e4a176b956260aa96a907ac65c37dd3eb357918d7/langpacks-3.0-21.amzn2023.0.4.src.rpm
```

### `rpm` package: `libICE-1.0.10-6.amzn2023.0.2.x86_64`

Licenses (from `rpm --query`): MIT

Source:

```console
$ dnf --quiet download --source --url libICE-1.0.10-6.amzn2023.0.2
https://cdn.amazonlinux.com/al2023/core/guids/78a1f37d281a9c8eb5115c4f9b2f8306b103426d1c252c1a59e532225ea7a73b/SRPMS/../../../../blobstore/58d8646d5b32ea42ef10e05fb569ac027ae80a6823394ea6bb06d6a6c55b748c/libICE-1.0.10-6.amzn2023.0.2.src.rpm
```

### `rpm` package: `libSM-1.2.3-8.amzn2023.0.2.x86_64`

Licenses (from `rpm --query`): MIT

Source:

```console
$ dnf --quiet download --source --url libSM-1.2.3-8.amzn2023.0.2
https://cdn.amazonlinux.com/al2023/core/guids/78a1f37d281a9c8eb5115c4f9b2f8306b103426d1c252c1a59e532225ea7a73b/SRPMS/../../../../blobstore/f9e9f75f9f1208c45c6cf569d24e190ddea8fadba96804240ce325854310d0d1/libSM-1.2.3-8.amzn2023.0.2.src.rpm
```

### `rpm` package: `libX11-1.7.2-3.amzn2023.0.4.x86_64`

Licenses (from `rpm --query`): MIT

Source:

```console
$ dnf --quiet download --source --url libX11-1.7.2-3.amzn2023.0.4
https://cdn.amazonlinux.com/al2023/core/guids/78a1f37d281a9c8eb5115c4f9b2f8306b103426d1c252c1a59e532225ea7a73b/SRPMS/../../../../blobstore/20428f5b854c36788b26eb7527a5cdfb708519871c3a745dcc5c9890b01f6bfa/libX11-1.7.2-3.amzn2023.0.4.src.rpm
```

### `rpm` package: `libX11-common-1.7.2-3.amzn2023.0.4.noarch`

Licenses (from `rpm --query`): MIT

Source:

```console
$ dnf --quiet download --source --url libX11-common-1.7.2-3.amzn2023.0.4.noarch
https://cdn.amazonlinux.com/al2023/core/guids/78a1f37d281a9c8eb5115c4f9b2f8306b103426d1c252c1a59e532225ea7a73b/SRPMS/../../../../blobstore/20428f5b854c36788b26eb7527a5cdfb708519871c3a745dcc5c9890b01f6bfa/libX11-1.7.2-3.amzn2023.0.4.src.rpm
```

### `rpm` package: `libXau-1.0.9-6.amzn2023.0.2.x86_64`

Licenses (from `rpm --query`): MIT

Source:

```console
$ dnf --quiet download --source --url libXau-1.0.9-6.amzn2023.0.2
https://cdn.amazonlinux.com/al2023/core/guids/78a1f37d281a9c8eb5115c4f9b2f8306b103426d1c252c1a59e532225ea7a73b/SRPMS/../../../../blobstore/38abae0f18aabd8e8c0b68a2ecdea1603509472d9861107b7482dc2edd5016dc/libXau-1.0.9-6.amzn2023.0.2.src.rpm
```

### `rpm` package: `libXext-1.3.4-6.amzn2023.0.2.x86_64`

Licenses (from `rpm --query`): MIT

Source:

```console
$ dnf --quiet download --source --url libXext-1.3.4-6.amzn2023.0.2
https://cdn.amazonlinux.com/al2023/core/guids/78a1f37d281a9c8eb5115c4f9b2f8306b103426d1c252c1a59e532225ea7a73b/SRPMS/../../../../blobstore/a7e8e5c1db4214a6b78989af3d58dceceb039c02d3b4f88cfd88b35b4b02ca88/libXext-1.3.4-6.amzn2023.0.2.src.rpm
```

### `rpm` package: `libXi-1.7.10-6.amzn2023.0.2.x86_64`

Licenses (from `rpm --query`): MIT

Source:

```console
$ dnf --quiet download --source --url libXi-1.7.10-6.amzn2023.0.2
https://cdn.amazonlinux.com/al2023/core/guids/78a1f37d281a9c8eb5115c4f9b2f8306b103426d1c252c1a59e532225ea7a73b/SRPMS/../../../../blobstore/19594fa2eae65889e6060740bd79191b002bcd21e7bfef4ea23a6960391aa896/libXi-1.7.10-6.amzn2023.0.2.src.rpm
```

### `rpm` package: `libXinerama-1.1.4-8.amzn2023.0.2.x86_64`

Licenses (from `rpm --query`): MIT

Source:

```console
$ dnf --quiet download --source --url libXinerama-1.1.4-8.amzn2023.0.2
https://cdn.amazonlinux.com/al2023/core/guids/78a1f37d281a9c8eb5115c4f9b2f8306b103426d1c252c1a59e532225ea7a73b/SRPMS/../../../../blobstore/f029205f979be21aa8f2bd691fff1210d7d8f242a567742197e147757b2c1799/libXinerama-1.1.4-8.amzn2023.0.2.src.rpm
```

### `rpm` package: `libXrandr-1.5.2-6.amzn2023.0.2.x86_64`

Licenses (from `rpm --query`): MIT

Source:

```console
$ dnf --quiet download --source --url libXrandr-1.5.2-6.amzn2023.0.2
https://cdn.amazonlinux.com/al2023/core/guids/78a1f37d281a9c8eb5115c4f9b2f8306b103426d1c252c1a59e532225ea7a73b/SRPMS/../../../../blobstore/38c4966b9aafcefb0464ed8c5156e299f842e1a8fb953c93d160c177d1e33cfa/libXrandr-1.5.2-6.amzn2023.0.2.src.rpm
```

### `rpm` package: `libXrender-0.9.10-14.amzn2023.0.2.x86_64`

Licenses (from `rpm --query`): MIT

Source:

```console
$ dnf --quiet download --source --url libXrender-0.9.10-14.amzn2023.0.2
https://cdn.amazonlinux.com/al2023/core/guids/78a1f37d281a9c8eb5115c4f9b2f8306b103426d1c252c1a59e532225ea7a73b/SRPMS/../../../../blobstore/7b8f644e3ee7a7355cc04ee6e0c593bf1ef70e4c53f18d831d526a33294a0909/libXrender-0.9.10-14.amzn2023.0.2.src.rpm
```

### `rpm` package: `libXt-1.2.0-4.amzn2023.0.2.x86_64`

Licenses (from `rpm --query`): MIT

Source:

```console
$ dnf --quiet download --source --url libXt-1.2.0-4.amzn2023.0.2
https://cdn.amazonlinux.com/al2023/core/guids/78a1f37d281a9c8eb5115c4f9b2f8306b103426d1c252c1a59e532225ea7a73b/SRPMS/../../../../blobstore/b94074be3e52b497b09c73b85416245359d1b6370db7d4bf4324fd035d5cf9b6/libXt-1.2.0-4.amzn2023.0.2.src.rpm
```

### `rpm` package: `libXtst-1.2.3-14.amzn2023.0.2.x86_64`

Licenses (from `rpm --query`): MIT

Source:

```console
$ dnf --quiet download --source --url libXtst-1.2.3-14.amzn2023.0.2
https://cdn.amazonlinux.com/al2023/core/guids/78a1f37d281a9c8eb5115c4f9b2f8306b103426d1c252c1a59e532225ea7a73b/SRPMS/../../../../blobstore/6ad7b36dc497c7c2b8a27523ec1989f462e093e9a3fdd40164df0fd81f9e103e/libXtst-1.2.3-14.amzn2023.0.2.src.rpm
```

### `rpm` package: `libacl-2.3.1-2.amzn2023.0.2.x86_64`

Licenses (from `rpm --query`): LGPLv2+

Source:

```console
$ dnf --quiet download --source --url libacl-2.3.1-2.amzn2023.0.2
https://cdn.amazonlinux.com/al2023/core/guids/78a1f37d281a9c8eb5115c4f9b2f8306b103426d1c252c1a59e532225ea7a73b/SRPMS/../../../../blobstore/abffc134a517b95c6933dafd2d93596ab7eaf8b5a0a73f3954b9011526471911/acl-2.3.1-2.amzn2023.0.2.src.rpm
```

### `rpm` package: `libarchive-3.5.3-2.amzn2023.0.3.x86_64`

Licenses (from `rpm --query`): BSD

Source:

```console
$ dnf --quiet download --source --url libarchive-3.5.3-2.amzn2023.0.3
https://cdn.amazonlinux.com/al2023/core/guids/78a1f37d281a9c8eb5115c4f9b2f8306b103426d1c252c1a59e532225ea7a73b/SRPMS/../../../../blobstore/85a08d330e925e69650eb46afe329413737d885e774d2aa86246e35bf3f53c1b/libarchive-3.5.3-2.amzn2023.0.3.src.rpm
```

### `rpm` package: `libassuan-2.5.5-1.amzn2023.0.2.x86_64`

Licenses (from `rpm --query`): LGPLv2+ and GPLv3+

Source:

```console
$ dnf --quiet download --source --url libassuan-2.5.5-1.amzn2023.0.2
https://cdn.amazonlinux.com/al2023/core/guids/78a1f37d281a9c8eb5115c4f9b2f8306b103426d1c252c1a59e532225ea7a73b/SRPMS/../../../../blobstore/e76d29fe0fa8402c9d9ce3130a5c17c21184e64f48e422c291e0a2c796dbe048/libassuan-2.5.5-1.amzn2023.0.2.src.rpm
```

### `rpm` package: `libattr-2.5.1-3.amzn2023.0.2.x86_64`

Licenses (from `rpm --query`): LGPLv2+

Source:

```console
$ dnf --quiet download --source --url libattr-2.5.1-3.amzn2023.0.2
https://cdn.amazonlinux.com/al2023/core/guids/78a1f37d281a9c8eb5115c4f9b2f8306b103426d1c252c1a59e532225ea7a73b/SRPMS/../../../../blobstore/5f96d4cbc2a467f87c4371434e516671b2ea05a3d9a52f2afa6c8c6536af087a/attr-2.5.1-3.amzn2023.0.2.src.rpm
```

### `rpm` package: `libblkid-2.37.4-1.amzn2023.0.4.x86_64`

Licenses (from `rpm --query`): LGPLv2+

Source:

```console
$ dnf --quiet download --source --url libblkid-2.37.4-1.amzn2023.0.4
https://cdn.amazonlinux.com/al2023/core/guids/78a1f37d281a9c8eb5115c4f9b2f8306b103426d1c252c1a59e532225ea7a73b/SRPMS/../../../../blobstore/5d583f3af0bebf693cbcb5e1f135d0a51449617aa1870faf1704d95a94b70402/util-linux-2.37.4-1.amzn2023.0.4.src.rpm
```

### `rpm` package: `libbrotli-1.0.9-4.amzn2023.0.2.x86_64`

Licenses (from `rpm --query`): MIT

Source:

```console
$ dnf --quiet download --source --url libbrotli-1.0.9-4.amzn2023.0.2
https://cdn.amazonlinux.com/al2023/core/guids/78a1f37d281a9c8eb5115c4f9b2f8306b103426d1c252c1a59e532225ea7a73b/SRPMS/../../../../blobstore/ae015da01f456a97b4738233cea3c8abcc9bfbcddd0890d3a60792d52d3a1497/brotli-1.0.9-4.amzn2023.0.2.src.rpm
```

### `rpm` package: `libcap-2.48-2.amzn2023.0.3.x86_64`

Licenses (from `rpm --query`): BSD or GPLv2

Source:

```console
$ dnf --quiet download --source --url libcap-2.48-2.amzn2023.0.3
https://cdn.amazonlinux.com/al2023/core/guids/78a1f37d281a9c8eb5115c4f9b2f8306b103426d1c252c1a59e532225ea7a73b/SRPMS/../../../../blobstore/2e0261f9c0510e9f685fad06a49a0c1a3efffa6ddcc5a5240a0546ea34eadffa/libcap-2.48-2.amzn2023.0.3.src.rpm
```

### `rpm` package: `libcap-ng-0.8.2-4.amzn2023.0.2.x86_64`

Licenses (from `rpm --query`): LGPLv2+

Source:

```console
$ dnf --quiet download --source --url libcap-ng-0.8.2-4.amzn2023.0.2
https://cdn.amazonlinux.com/al2023/core/guids/78a1f37d281a9c8eb5115c4f9b2f8306b103426d1c252c1a59e532225ea7a73b/SRPMS/../../../../blobstore/5c78d25798270772d690e2d3e8de8388d988dcbe2bf183172e490fa47b78ec79/libcap-ng-0.8.2-4.amzn2023.0.2.src.rpm
```

### `rpm` package: `libcom_err-1.46.5-2.amzn2023.0.2.x86_64`

Licenses (from `rpm --query`): MIT

Source:

```console
$ dnf --quiet download --source --url libcom_err-1.46.5-2.amzn2023.0.2
https://cdn.amazonlinux.com/al2023/core/guids/78a1f37d281a9c8eb5115c4f9b2f8306b103426d1c252c1a59e532225ea7a73b/SRPMS/../../../../blobstore/1bd46590cfe3a4600a72bb0cc0677d5f22e2c25cf765b722f26b5f3239ef8813/e2fsprogs-1.46.5-2.amzn2023.0.2.src.rpm
```

### `rpm` package: `libcomps-0.1.20-1.amzn2023.x86_64`

Licenses (from `rpm --query`): GPL-2.0-or-later

Source:

```console
$ dnf --quiet download --source --url libcomps-0.1.20-1.amzn2023
https://cdn.amazonlinux.com/al2023/core/guids/78a1f37d281a9c8eb5115c4f9b2f8306b103426d1c252c1a59e532225ea7a73b/SRPMS/../../../../blobstore/2c60a977f6060dee6b1b1801f9ba36cb52d0726e5be1d1f8759d72fee63971af/libcomps-0.1.20-1.amzn2023.src.rpm
```

### `rpm` package: `libcurl-minimal-8.5.0-1.amzn2023.0.4.x86_64`

Licenses (from `rpm --query`): curl

Source:

```console
$ dnf --quiet download --source --url libcurl-minimal-8.5.0-1.amzn2023.0.4
https://cdn.amazonlinux.com/al2023/core/guids/78a1f37d281a9c8eb5115c4f9b2f8306b103426d1c252c1a59e532225ea7a73b/SRPMS/../../../../blobstore/06df1530ceda85d884d0fd3ccf87402e9c3b56125f93d8bec8b96cc75f15c5c8/curl-8.5.0-1.amzn2023.0.4.src.rpm
```

### `rpm` package: `libdnf-0.69.0-8.amzn2023.0.5.x86_64`

Licenses (from `rpm --query`): LGPLv2+

Source:

```console
$ dnf --quiet download --source --url libdnf-0.69.0-8.amzn2023.0.5
https://cdn.amazonlinux.com/al2023/core/guids/78a1f37d281a9c8eb5115c4f9b2f8306b103426d1c252c1a59e532225ea7a73b/SRPMS/../../../../blobstore/59cc9ff8c6220c422fe83eb7371d7c67091e4dc2f13f7d23314553027592e6c9/libdnf-0.69.0-8.amzn2023.0.5.src.rpm
```

### `rpm` package: `libffi-3.4.4-1.amzn2023.0.1.x86_64`

Licenses (from `rpm --query`): MIT

Source:

```console
$ dnf --quiet download --source --url libffi-3.4.4-1.amzn2023.0.1
https://cdn.amazonlinux.com/al2023/core/guids/78a1f37d281a9c8eb5115c4f9b2f8306b103426d1c252c1a59e532225ea7a73b/SRPMS/../../../../blobstore/dd62668d8185eb8077c6b6305913b450519b2d366a2b19e2f60fe085a84e91f0/libffi-3.4.4-1.amzn2023.0.1.src.rpm
```

### `rpm` package: `libgcc-11.4.1-2.amzn2023.0.2.x86_64`

Licenses (from `rpm --query`): GPLv3+ and GPLv3+ with exceptions and GPLv2+ with exceptions and LGPLv2+ and BSD

Source:

```console
$ dnf --quiet download --source --url libgcc-11.4.1-2.amzn2023.0.2
https://cdn.amazonlinux.com/al2023/core/guids/78a1f37d281a9c8eb5115c4f9b2f8306b103426d1c252c1a59e532225ea7a73b/SRPMS/../../../../blobstore/2073edf2726912f6a20a519265f9516f8d28597593a4a51d98fbfebf82c0f283/gcc-11.4.1-2.amzn2023.0.2.src.rpm
```

### `rpm` package: `libgcrypt-1.10.2-1.amzn2023.0.1.x86_64`

Licenses (from `rpm --query`): LGPLv2+

Source:

```console
$ dnf --quiet download --source --url libgcrypt-1.10.2-1.amzn2023.0.1
https://cdn.amazonlinux.com/al2023/core/guids/78a1f37d281a9c8eb5115c4f9b2f8306b103426d1c252c1a59e532225ea7a73b/SRPMS/../../../../blobstore/a6bee3b6da6cf71b898c1621c9104cd11bf3b3970b05d0fa39ebdb4a0342cce0/libgcrypt-1.10.2-1.amzn2023.0.1.src.rpm
```

### `rpm` package: `libgomp-11.4.1-2.amzn2023.0.2.x86_64`

Licenses (from `rpm --query`): GPLv3+ and GPLv3+ with exceptions and GPLv2+ with exceptions and LGPLv2+ and BSD

Source:

```console
$ dnf --quiet download --source --url libgomp-11.4.1-2.amzn2023.0.2
https://cdn.amazonlinux.com/al2023/core/guids/78a1f37d281a9c8eb5115c4f9b2f8306b103426d1c252c1a59e532225ea7a73b/SRPMS/../../../../blobstore/2073edf2726912f6a20a519265f9516f8d28597593a4a51d98fbfebf82c0f283/gcc-11.4.1-2.amzn2023.0.2.src.rpm
```

### `rpm` package: `libgpg-error-1.42-1.amzn2023.0.2.x86_64`

Licenses (from `rpm --query`): LGPLv2+

Source:

```console
$ dnf --quiet download --source --url libgpg-error-1.42-1.amzn2023.0.2
https://cdn.amazonlinux.com/al2023/core/guids/78a1f37d281a9c8eb5115c4f9b2f8306b103426d1c252c1a59e532225ea7a73b/SRPMS/../../../../blobstore/4851a17077c481764d8a2a776da1e07bc39b5766f101d23c27b8bd6ee8fd7f4d/libgpg-error-1.42-1.amzn2023.0.2.src.rpm
```

### `rpm` package: `libidn2-2.3.2-1.amzn2023.0.5.x86_64`

Licenses (from `rpm --query`): (GPLv2+ or LGPLv3+) and GPLv3+

Source:

```console
$ dnf --quiet download --source --url libidn2-2.3.2-1.amzn2023.0.5
https://cdn.amazonlinux.com/al2023/core/guids/78a1f37d281a9c8eb5115c4f9b2f8306b103426d1c252c1a59e532225ea7a73b/SRPMS/../../../../blobstore/609a72da4b90a6f582440a3905f728f4bba20fb8599a622613def09255370165/libidn2-2.3.2-1.amzn2023.0.5.src.rpm
```

### `rpm` package: `libjpeg-turbo-2.1.4-2.amzn2023.0.5.x86_64`

Licenses (from `rpm --query`): IJG

Source:

```console
$ dnf --quiet download --source --url libjpeg-turbo-2.1.4-2.amzn2023.0.5
https://cdn.amazonlinux.com/al2023/core/guids/78a1f37d281a9c8eb5115c4f9b2f8306b103426d1c252c1a59e532225ea7a73b/SRPMS/../../../../blobstore/3b69c82120b8e0dc45c3391f8e9eacb5d3711e9c7f7c448f258fa0fbde4417ad/libjpeg-turbo-2.1.4-2.amzn2023.0.5.src.rpm
```

### `rpm` package: `libmodulemd-2.13.0-2.amzn2023.0.2.x86_64`

Licenses (from `rpm --query`): MIT

Source:

```console
$ dnf --quiet download --source --url libmodulemd-2.13.0-2.amzn2023.0.2
https://cdn.amazonlinux.com/al2023/core/guids/78a1f37d281a9c8eb5115c4f9b2f8306b103426d1c252c1a59e532225ea7a73b/SRPMS/../../../../blobstore/0981e43a27a8e154d4882fcfdc346e6be4429f95f23505b56e6f161ce32b7794/libmodulemd-2.13.0-2.amzn2023.0.2.src.rpm
```

### `rpm` package: `libmount-2.37.4-1.amzn2023.0.4.x86_64`

Licenses (from `rpm --query`): LGPLv2+

Source:

```console
$ dnf --quiet download --source --url libmount-2.37.4-1.amzn2023.0.4
https://cdn.amazonlinux.com/al2023/core/guids/78a1f37d281a9c8eb5115c4f9b2f8306b103426d1c252c1a59e532225ea7a73b/SRPMS/../../../../blobstore/5d583f3af0bebf693cbcb5e1f135d0a51449617aa1870faf1704d95a94b70402/util-linux-2.37.4-1.amzn2023.0.4.src.rpm
```

### `rpm` package: `libnghttp2-1.59.0-3.amzn2023.0.1.x86_64`

Licenses (from `rpm --query`): MIT

Source:

```console
$ dnf --quiet download --source --url libnghttp2-1.59.0-3.amzn2023.0.1
https://cdn.amazonlinux.com/al2023/core/guids/78a1f37d281a9c8eb5115c4f9b2f8306b103426d1c252c1a59e532225ea7a73b/SRPMS/../../../../blobstore/0d407b31e17cfe06f1e29e212235632374a3155517e855656492ecfe307f5eef/nghttp2-1.59.0-3.amzn2023.0.1.src.rpm
```

### `rpm` package: `libpng-1.6.37-10.amzn2023.0.6.x86_64`

Licenses (from `rpm --query`): zlib

Source:

```console
$ dnf --quiet download --source --url libpng-1.6.37-10.amzn2023.0.6
https://cdn.amazonlinux.com/al2023/core/guids/78a1f37d281a9c8eb5115c4f9b2f8306b103426d1c252c1a59e532225ea7a73b/SRPMS/../../../../blobstore/d92ca3c3813afb2f4966fb2d52402eb49c1e6130c67b52a8ed8eab4a30415ad6/libpng-1.6.37-10.amzn2023.0.6.src.rpm
```

### `rpm` package: `libpsl-0.21.1-3.amzn2023.0.2.x86_64`

Licenses (from `rpm --query`): MIT

Source:

```console
$ dnf --quiet download --source --url libpsl-0.21.1-3.amzn2023.0.2
https://cdn.amazonlinux.com/al2023/core/guids/78a1f37d281a9c8eb5115c4f9b2f8306b103426d1c252c1a59e532225ea7a73b/SRPMS/../../../../blobstore/49f3ad733c92ca4b6f0a2eff2df4d2f4ee54028af53f8a2557e5169bd1ceb3f1/libpsl-0.21.1-3.amzn2023.0.2.src.rpm
```

### `rpm` package: `librepo-1.14.5-2.amzn2023.0.1.x86_64`

Licenses (from `rpm --query`): LGPLv2+

Source:

```console
$ dnf --quiet download --source --url librepo-1.14.5-2.amzn2023.0.1
https://cdn.amazonlinux.com/al2023/core/guids/78a1f37d281a9c8eb5115c4f9b2f8306b103426d1c252c1a59e532225ea7a73b/SRPMS/../../../../blobstore/0a0f87fd1b750bc280576311c38be43fd40a0f1b824a3208a2a88ec180c020fa/librepo-1.14.5-2.amzn2023.0.1.src.rpm
```

### `rpm` package: `libreport-filesystem-2.15.2-2.amzn2023.0.2.noarch`

Licenses (from `rpm --query`): GPLv2+

Source:

```console
$ dnf --quiet download --source --url libreport-filesystem-2.15.2-2.amzn2023.0.2.noarch
https://cdn.amazonlinux.com/al2023/core/guids/78a1f37d281a9c8eb5115c4f9b2f8306b103426d1c252c1a59e532225ea7a73b/SRPMS/../../../../blobstore/9321ff29e6caeb5d54f7a85179d286bb0ca55008991b0ddd1b0dbb3e36e607c4/libreport-2.15.2-2.amzn2023.0.2.src.rpm
```

### `rpm` package: `libselinux-3.4-5.amzn2023.0.2.x86_64`

Licenses (from `rpm --query`): Public Domain

Source:

```console
$ dnf --quiet download --source --url libselinux-3.4-5.amzn2023.0.2
https://cdn.amazonlinux.com/al2023/core/guids/78a1f37d281a9c8eb5115c4f9b2f8306b103426d1c252c1a59e532225ea7a73b/SRPMS/../../../../blobstore/3edd36f0d73ba1e9b08cf3ab73865b3b555111944103cd8e99edf4b71048d804/libselinux-3.4-5.amzn2023.0.2.src.rpm
```

### `rpm` package: `libsepol-3.4-3.amzn2023.0.3.x86_64`

Licenses (from `rpm --query`): LGPLv2+

Source:

```console
$ dnf --quiet download --source --url libsepol-3.4-3.amzn2023.0.3
https://cdn.amazonlinux.com/al2023/core/guids/78a1f37d281a9c8eb5115c4f9b2f8306b103426d1c252c1a59e532225ea7a73b/SRPMS/../../../../blobstore/9fb43af9fbea04646a759147d038e029a0568cab2191d5ae7ba2363ccd10dd9f/libsepol-3.4-3.amzn2023.0.3.src.rpm
```

### `rpm` package: `libsigsegv-2.13-2.amzn2023.0.2.x86_64`

Licenses (from `rpm --query`): GPLv2+

Source:

```console
$ dnf --quiet download --source --url libsigsegv-2.13-2.amzn2023.0.2
https://cdn.amazonlinux.com/al2023/core/guids/78a1f37d281a9c8eb5115c4f9b2f8306b103426d1c252c1a59e532225ea7a73b/SRPMS/../../../../blobstore/18a5131e075b467fda622c30e0f96787c39d18ed130a0d52aeed7eff388cd7d1/libsigsegv-2.13-2.amzn2023.0.2.src.rpm
```

### `rpm` package: `libsmartcols-2.37.4-1.amzn2023.0.4.x86_64`

Licenses (from `rpm --query`): LGPLv2+

Source:

```console
$ dnf --quiet download --source --url libsmartcols-2.37.4-1.amzn2023.0.4
https://cdn.amazonlinux.com/al2023/core/guids/78a1f37d281a9c8eb5115c4f9b2f8306b103426d1c252c1a59e532225ea7a73b/SRPMS/../../../../blobstore/5d583f3af0bebf693cbcb5e1f135d0a51449617aa1870faf1704d95a94b70402/util-linux-2.37.4-1.amzn2023.0.4.src.rpm
```

### `rpm` package: `libsolv-0.7.22-1.amzn2023.0.2.x86_64`

Licenses (from `rpm --query`): BSD

Source:

```console
$ dnf --quiet download --source --url libsolv-0.7.22-1.amzn2023.0.2
https://cdn.amazonlinux.com/al2023/core/guids/78a1f37d281a9c8eb5115c4f9b2f8306b103426d1c252c1a59e532225ea7a73b/SRPMS/../../../../blobstore/b85c93b65c74bfbbb45e29a0fea409d38d8893cbb483684e2175357820273ff3/libsolv-0.7.22-1.amzn2023.0.2.src.rpm
```

### `rpm` package: `libstdc++-11.4.1-2.amzn2023.0.2.x86_64`

Licenses (from `rpm --query`): GPLv3+ and GPLv3+ with exceptions and GPLv2+ with exceptions and LGPLv2+ and BSD

Source:

```console
$ dnf --quiet download --source --url libstdc++-11.4.1-2.amzn2023.0.2
https://cdn.amazonlinux.com/al2023/core/guids/78a1f37d281a9c8eb5115c4f9b2f8306b103426d1c252c1a59e532225ea7a73b/SRPMS/../../../../blobstore/2073edf2726912f6a20a519265f9516f8d28597593a4a51d98fbfebf82c0f283/gcc-11.4.1-2.amzn2023.0.2.src.rpm
```

### `rpm` package: `libtasn1-4.19.0-1.amzn2023.0.4.x86_64`

Licenses (from `rpm --query`): GPLv3+ and LGPLv2+

Source:

```console
$ dnf --quiet download --source --url libtasn1-4.19.0-1.amzn2023.0.4
https://cdn.amazonlinux.com/al2023/core/guids/78a1f37d281a9c8eb5115c4f9b2f8306b103426d1c252c1a59e532225ea7a73b/SRPMS/../../../../blobstore/16fd2f1f381f9c740be2b592e421ed187962bef2a8b09bc51ac311aa2f8d6f87/libtasn1-4.19.0-1.amzn2023.0.4.src.rpm
```

### `rpm` package: `libunistring-0.9.10-10.amzn2023.0.2.x86_64`

Licenses (from `rpm --query`): GPLV2+ or LGPLv3+

Source:

```console
$ dnf --quiet download --source --url libunistring-0.9.10-10.amzn2023.0.2
https://cdn.amazonlinux.com/al2023/core/guids/78a1f37d281a9c8eb5115c4f9b2f8306b103426d1c252c1a59e532225ea7a73b/SRPMS/../../../../blobstore/df2b927b122a4a9c6dd18caa7688ab5e0b3b88b17b0671c3fe2baa1ca3b3da17/libunistring-0.9.10-10.amzn2023.0.2.src.rpm
```

### `rpm` package: `libuuid-2.37.4-1.amzn2023.0.4.x86_64`

Licenses (from `rpm --query`): BSD

Source:

```console
$ dnf --quiet download --source --url libuuid-2.37.4-1.amzn2023.0.4
https://cdn.amazonlinux.com/al2023/core/guids/78a1f37d281a9c8eb5115c4f9b2f8306b103426d1c252c1a59e532225ea7a73b/SRPMS/../../../../blobstore/5d583f3af0bebf693cbcb5e1f135d0a51449617aa1870faf1704d95a94b70402/util-linux-2.37.4-1.amzn2023.0.4.src.rpm
```

### `rpm` package: `libverto-0.3.2-1.amzn2023.0.2.x86_64`

Licenses (from `rpm --query`): MIT

Source:

```console
$ dnf --quiet download --source --url libverto-0.3.2-1.amzn2023.0.2
https://cdn.amazonlinux.com/al2023/core/guids/78a1f37d281a9c8eb5115c4f9b2f8306b103426d1c252c1a59e532225ea7a73b/SRPMS/../../../../blobstore/69471fc8822dfc2d2453f7bfc252ba7a7587600659daa1674065e8cb8dcb99a2/libverto-0.3.2-1.amzn2023.0.2.src.rpm
```

### `rpm` package: `libxcb-1.13.1-7.amzn2023.0.2.x86_64`

Licenses (from `rpm --query`): MIT

Source:

```console
$ dnf --quiet download --source --url libxcb-1.13.1-7.amzn2023.0.2
https://cdn.amazonlinux.com/al2023/core/guids/78a1f37d281a9c8eb5115c4f9b2f8306b103426d1c252c1a59e532225ea7a73b/SRPMS/../../../../blobstore/8c9d020573ab70c2ff03974ab70e5d07ac8437e96dbdd632e88378c5b70d4a07/libxcb-1.13.1-7.amzn2023.0.2.src.rpm
```

### `rpm` package: `libxcrypt-4.4.33-7.amzn2023.x86_64`

Licenses (from `rpm --query`): LGPL-2.1-or-later AND BSD-3-Clause AND BSD-2-Clause AND BSD-2-Clause-FreeBSD AND 0BSD AND CC0-1.0 AND LicenseRef-Fedora-Public-Domain

Source:

```console
$ dnf --quiet download --source --url libxcrypt-4.4.33-7.amzn2023
https://cdn.amazonlinux.com/al2023/core/guids/78a1f37d281a9c8eb5115c4f9b2f8306b103426d1c252c1a59e532225ea7a73b/SRPMS/../../../../blobstore/15ec09ebcdac3bc32e7ede1ac2926be1722c05016a9b62d0be4e0cadcbfa1080/libxcrypt-4.4.33-7.amzn2023.src.rpm
```

### `rpm` package: `libxml2-2.10.4-1.amzn2023.0.6.x86_64`

Licenses (from `rpm --query`): MIT

Source:

```console
$ dnf --quiet download --source --url libxml2-2.10.4-1.amzn2023.0.6
https://cdn.amazonlinux.com/al2023/core/guids/78a1f37d281a9c8eb5115c4f9b2f8306b103426d1c252c1a59e532225ea7a73b/SRPMS/../../../../blobstore/d65ad7e14a134d1367dfd8a333a0358a90d0bc8ef7e436d0a982feaab8a8b856/libxml2-2.10.4-1.amzn2023.0.6.src.rpm
```

### `rpm` package: `libyaml-0.2.5-5.amzn2023.0.2.x86_64`

Licenses (from `rpm --query`): MIT

Source:

```console
$ dnf --quiet download --source --url libyaml-0.2.5-5.amzn2023.0.2
https://cdn.amazonlinux.com/al2023/core/guids/78a1f37d281a9c8eb5115c4f9b2f8306b103426d1c252c1a59e532225ea7a73b/SRPMS/../../../../blobstore/c880c393ba32929284579c71f978582e5efe02c63acfbd5b87f189ec07faaa2f/libyaml-0.2.5-5.amzn2023.0.2.src.rpm
```

### `rpm` package: `libzstd-1.5.5-1.amzn2023.0.1.x86_64`

Licenses (from `rpm --query`): BSD and GPLv2

Source:

```console
$ dnf --quiet download --source --url libzstd-1.5.5-1.amzn2023.0.1
https://cdn.amazonlinux.com/al2023/core/guids/78a1f37d281a9c8eb5115c4f9b2f8306b103426d1c252c1a59e532225ea7a73b/SRPMS/../../../../blobstore/7b8eaa8999f8329c4253055d5b5d54b78907363dc4d512fd3deda46cd385efe7/zstd-1.5.5-1.amzn2023.0.1.src.rpm
```

### `rpm` package: `lua-libs-5.4.4-3.amzn2023.0.2.x86_64`

Licenses (from `rpm --query`): MIT

Source:

```console
$ dnf --quiet download --source --url lua-libs-5.4.4-3.amzn2023.0.2
https://cdn.amazonlinux.com/al2023/core/guids/78a1f37d281a9c8eb5115c4f9b2f8306b103426d1c252c1a59e532225ea7a73b/SRPMS/../../../../blobstore/4a157115ba2f4b568b7915073d1046770faf78b0ddde3b0f3d53abcbbf6d7088/lua-5.4.4-3.amzn2023.0.2.src.rpm
```

### `rpm` package: `lz4-libs-1.9.4-1.amzn2023.0.2.x86_64`

Licenses (from `rpm --query`): GPLv2+ and BSD

Source:

```console
$ dnf --quiet download --source --url lz4-libs-1.9.4-1.amzn2023.0.2
https://cdn.amazonlinux.com/al2023/core/guids/78a1f37d281a9c8eb5115c4f9b2f8306b103426d1c252c1a59e532225ea7a73b/SRPMS/../../../../blobstore/844b15b026f8d8503c2249adcf0e911c74e475fc0cf5e8d149d82bab194ca49a/lz4-1.9.4-1.amzn2023.0.2.src.rpm
```

### `rpm` package: `mpfr-4.1.0-7.amzn2023.0.2.x86_64`

Licenses (from `rpm --query`): LGPLv3+

Source:

```console
$ dnf --quiet download --source --url mpfr-4.1.0-7.amzn2023.0.2
https://cdn.amazonlinux.com/al2023/core/guids/78a1f37d281a9c8eb5115c4f9b2f8306b103426d1c252c1a59e532225ea7a73b/SRPMS/../../../../blobstore/2d8b4b3873d2d0120cc80ac6ce18c0e3effea624391149a1e61e692cc55b245a/mpfr-4.1.0-7.amzn2023.0.2.src.rpm
```

### `rpm` package: `ncurses-base-6.2-4.20200222.amzn2023.0.6.noarch`

Licenses (from `rpm --query`): MIT

Source:

```console
$ dnf --quiet download --source --url ncurses-base-6.2-4.20200222.amzn2023.0.6.noarch
https://cdn.amazonlinux.com/al2023/core/guids/78a1f37d281a9c8eb5115c4f9b2f8306b103426d1c252c1a59e532225ea7a73b/SRPMS/../../../../blobstore/10e94bd934aa393cf2f83bd21437f5208583051dbc4a53d394e33ed9d2a8cff2/ncurses-6.2-4.20200222.amzn2023.0.6.src.rpm
```

### `rpm` package: `ncurses-libs-6.2-4.20200222.amzn2023.0.6.x86_64`

Licenses (from `rpm --query`): MIT

Source:

```console
$ dnf --quiet download --source --url ncurses-libs-6.2-4.20200222.amzn2023.0.6
https://cdn.amazonlinux.com/al2023/core/guids/78a1f37d281a9c8eb5115c4f9b2f8306b103426d1c252c1a59e532225ea7a73b/SRPMS/../../../../blobstore/10e94bd934aa393cf2f83bd21437f5208583051dbc4a53d394e33ed9d2a8cff2/ncurses-6.2-4.20200222.amzn2023.0.6.src.rpm
```

### `rpm` package: `npth-1.6-6.amzn2023.0.2.x86_64`

Licenses (from `rpm --query`): LGPLv2+

Source:

```console
$ dnf --quiet download --source --url npth-1.6-6.amzn2023.0.2
https://cdn.amazonlinux.com/al2023/core/guids/78a1f37d281a9c8eb5115c4f9b2f8306b103426d1c252c1a59e532225ea7a73b/SRPMS/../../../../blobstore/61d865eda39cab60211e5d995683d912479e2a3abae07c4a1506b2c04c76ab47/npth-1.6-6.amzn2023.0.2.src.rpm
```

### `rpm` package: `openssl-libs-3.0.8-1.amzn2023.0.12.x86_64`

Licenses (from `rpm --query`): ASL 2.0

Source:

```console
$ dnf --quiet download --source --url openssl-libs-3.0.8-1.amzn2023.0.12
https://cdn.amazonlinux.com/al2023/core/guids/78a1f37d281a9c8eb5115c4f9b2f8306b103426d1c252c1a59e532225ea7a73b/SRPMS/../../../../blobstore/79993f88beeb5e7659c3b1ef554cd6e501a6bed5e93d2008d19e1e867ba64f1e/openssl-3.0.8-1.amzn2023.0.12.src.rpm
```

### `rpm` package: `p11-kit-0.24.1-2.amzn2023.0.3.x86_64`

Licenses (from `rpm --query`): BSD

Source:

```console
$ dnf --quiet download --source --url p11-kit-0.24.1-2.amzn2023.0.3
https://cdn.amazonlinux.com/al2023/core/guids/78a1f37d281a9c8eb5115c4f9b2f8306b103426d1c252c1a59e532225ea7a73b/SRPMS/../../../../blobstore/ae1ed1744168e6e3e7b6b463a39546de2f3558c925e83f644fde038dc918f77c/p11-kit-0.24.1-2.amzn2023.0.3.src.rpm
```

### `rpm` package: `p11-kit-trust-0.24.1-2.amzn2023.0.3.x86_64`

Licenses (from `rpm --query`): BSD

Source:

```console
$ dnf --quiet download --source --url p11-kit-trust-0.24.1-2.amzn2023.0.3
https://cdn.amazonlinux.com/al2023/core/guids/78a1f37d281a9c8eb5115c4f9b2f8306b103426d1c252c1a59e532225ea7a73b/SRPMS/../../../../blobstore/ae1ed1744168e6e3e7b6b463a39546de2f3558c925e83f644fde038dc918f77c/p11-kit-0.24.1-2.amzn2023.0.3.src.rpm
```

### `rpm` package: `pcre2-10.40-1.amzn2023.0.3.x86_64`

Licenses (from `rpm --query`): BSD

Source:

```console
$ dnf --quiet download --source --url pcre2-10.40-1.amzn2023.0.3
https://cdn.amazonlinux.com/al2023/core/guids/78a1f37d281a9c8eb5115c4f9b2f8306b103426d1c252c1a59e532225ea7a73b/SRPMS/../../../../blobstore/45e1170740316469029027eb3ec16f1f89999bdce964ab9e217c4397e7484fa0/pcre2-10.40-1.amzn2023.0.3.src.rpm
```

### `rpm` package: `pcre2-syntax-10.40-1.amzn2023.0.3.noarch`

Licenses (from `rpm --query`): BSD

Source:

```console
$ dnf --quiet download --source --url pcre2-syntax-10.40-1.amzn2023.0.3.noarch
https://cdn.amazonlinux.com/al2023/core/guids/78a1f37d281a9c8eb5115c4f9b2f8306b103426d1c252c1a59e532225ea7a73b/SRPMS/../../../../blobstore/45e1170740316469029027eb3ec16f1f89999bdce964ab9e217c4397e7484fa0/pcre2-10.40-1.amzn2023.0.3.src.rpm
```

### `rpm` package: `pixman-0.40.0-3.amzn2023.0.3.x86_64`

Licenses (from `rpm --query`): MIT

Source:

```console
$ dnf --quiet download --source --url pixman-0.40.0-3.amzn2023.0.3
https://cdn.amazonlinux.com/al2023/core/guids/78a1f37d281a9c8eb5115c4f9b2f8306b103426d1c252c1a59e532225ea7a73b/SRPMS/../../../../blobstore/5154a8133881bf1471cce361f21d9912da21bda85a2d60cc9f20e20c52335d1e/pixman-0.40.0-3.amzn2023.0.3.src.rpm
```

### `rpm` package: `popt-1.18-6.amzn2023.0.2.x86_64`

Licenses (from `rpm --query`): MIT

Source:

```console
$ dnf --quiet download --source --url popt-1.18-6.amzn2023.0.2
https://cdn.amazonlinux.com/al2023/core/guids/78a1f37d281a9c8eb5115c4f9b2f8306b103426d1c252c1a59e532225ea7a73b/SRPMS/../../../../blobstore/fd5f13b673439dd74792c2dd8094dff527f0e555df16063e599d6a0648fc1d81/popt-1.18-6.amzn2023.0.2.src.rpm
```

### `rpm` package: `publicsuffix-list-dafsa-20240212-61.amzn2023.noarch`

Licenses (from `rpm --query`): MPLv2.0

Source:

```console
$ dnf --quiet download --source --url publicsuffix-list-dafsa-20240212-61.amzn2023.noarch
https://cdn.amazonlinux.com/al2023/core/guids/78a1f37d281a9c8eb5115c4f9b2f8306b103426d1c252c1a59e532225ea7a73b/SRPMS/../../../../blobstore/4a68a866dff127861af4fd61ce706773b549769b514cd3e7314d955367e14b68/publicsuffix-list-20240212-61.amzn2023.src.rpm
```

### `rpm` package: `python3-3.9.16-1.amzn2023.0.8.x86_64`

Licenses (from `rpm --query`): Python

Source:

```console
$ dnf --quiet download --source --url python3-3.9.16-1.amzn2023.0.8
https://cdn.amazonlinux.com/al2023/core/guids/78a1f37d281a9c8eb5115c4f9b2f8306b103426d1c252c1a59e532225ea7a73b/SRPMS/../../../../blobstore/3cd8c96ededb043f4e3cedf143487b427d675f92d96a6e62c0c2f7814e0704a3/python3.9-3.9.16-1.amzn2023.0.8.src.rpm
```

### `rpm` package: `python3-dnf-4.14.0-1.amzn2023.0.5.noarch`

Licenses (from `rpm --query`): GPLv2+

Source:

```console
$ dnf --quiet download --source --url python3-dnf-4.14.0-1.amzn2023.0.5.noarch
https://cdn.amazonlinux.com/al2023/core/guids/78a1f37d281a9c8eb5115c4f9b2f8306b103426d1c252c1a59e532225ea7a73b/SRPMS/../../../../blobstore/3c7a286acf75f92e2600171b3b97237f9db9bf5b9466013b3c1686501ad6e7cd/dnf-4.14.0-1.amzn2023.0.5.src.rpm
```

### `rpm` package: `python3-gpg-1.15.1-6.amzn2023.0.3.x86_64`

Licenses (from `rpm --query`): LGPLv2+

Source:

```console
$ dnf --quiet download --source --url python3-gpg-1.15.1-6.amzn2023.0.3
https://cdn.amazonlinux.com/al2023/core/guids/78a1f37d281a9c8eb5115c4f9b2f8306b103426d1c252c1a59e532225ea7a73b/SRPMS/../../../../blobstore/99fedbc2cb2281dee4a51cbf47ec00c853e5f3e345135cd3c7a6a9424a9eb316/gpgme-1.15.1-6.amzn2023.0.3.src.rpm
```

### `rpm` package: `python3-hawkey-0.69.0-8.amzn2023.0.5.x86_64`

Licenses (from `rpm --query`): LGPLv2+

Source:

```console
$ dnf --quiet download --source --url python3-hawkey-0.69.0-8.amzn2023.0.5
https://cdn.amazonlinux.com/al2023/core/guids/78a1f37d281a9c8eb5115c4f9b2f8306b103426d1c252c1a59e532225ea7a73b/SRPMS/../../../../blobstore/59cc9ff8c6220c422fe83eb7371d7c67091e4dc2f13f7d23314553027592e6c9/libdnf-0.69.0-8.amzn2023.0.5.src.rpm
```

### `rpm` package: `python3-libcomps-0.1.20-1.amzn2023.x86_64`

Licenses (from `rpm --query`): GPL-2.0-or-later

Source:

```console
$ dnf --quiet download --source --url python3-libcomps-0.1.20-1.amzn2023
https://cdn.amazonlinux.com/al2023/core/guids/78a1f37d281a9c8eb5115c4f9b2f8306b103426d1c252c1a59e532225ea7a73b/SRPMS/../../../../blobstore/2c60a977f6060dee6b1b1801f9ba36cb52d0726e5be1d1f8759d72fee63971af/libcomps-0.1.20-1.amzn2023.src.rpm
```

### `rpm` package: `python3-libdnf-0.69.0-8.amzn2023.0.5.x86_64`

Licenses (from `rpm --query`): LGPLv2+

Source:

```console
$ dnf --quiet download --source --url python3-libdnf-0.69.0-8.amzn2023.0.5
https://cdn.amazonlinux.com/al2023/core/guids/78a1f37d281a9c8eb5115c4f9b2f8306b103426d1c252c1a59e532225ea7a73b/SRPMS/../../../../blobstore/59cc9ff8c6220c422fe83eb7371d7c67091e4dc2f13f7d23314553027592e6c9/libdnf-0.69.0-8.amzn2023.0.5.src.rpm
```

### `rpm` package: `python3-libs-3.9.16-1.amzn2023.0.8.x86_64`

Licenses (from `rpm --query`): Python

Source:

```console
$ dnf --quiet download --source --url python3-libs-3.9.16-1.amzn2023.0.8
https://cdn.amazonlinux.com/al2023/core/guids/78a1f37d281a9c8eb5115c4f9b2f8306b103426d1c252c1a59e532225ea7a73b/SRPMS/../../../../blobstore/3cd8c96ededb043f4e3cedf143487b427d675f92d96a6e62c0c2f7814e0704a3/python3.9-3.9.16-1.amzn2023.0.8.src.rpm
```

### `rpm` package: `python3-pip-wheel-21.3.1-2.amzn2023.0.7.noarch`

Licenses (from `rpm --query`): MIT and Python and ASL 2.0 and BSD and ISC and LGPLv2 and MPLv2.0 and (ASL 2.0 or BSD)

Source:

```console
$ dnf --quiet download --source --url python3-pip-wheel-21.3.1-2.amzn2023.0.7.noarch
https://cdn.amazonlinux.com/al2023/core/guids/78a1f37d281a9c8eb5115c4f9b2f8306b103426d1c252c1a59e532225ea7a73b/SRPMS/../../../../blobstore/65aa5dfbbcd011391bf2ea6926688b5b1cd1021eef3c92b35961da12bf95f827/python-pip-21.3.1-2.amzn2023.0.7.src.rpm
```

### `rpm` package: `python3-rpm-4.16.1.3-29.amzn2023.0.6.x86_64`

Licenses (from `rpm --query`): GPLv2+

Source:

```console
$ dnf --quiet download --source --url python3-rpm-4.16.1.3-29.amzn2023.0.6
https://cdn.amazonlinux.com/al2023/core/guids/78a1f37d281a9c8eb5115c4f9b2f8306b103426d1c252c1a59e532225ea7a73b/SRPMS/../../../../blobstore/2527ab9e1825bc6ad87e881431c9245a260dfaae70d820a8769dcb4f2cb38abc/rpm-4.16.1.3-29.amzn2023.0.6.src.rpm
```

### `rpm` package: `python3-setuptools-wheel-59.6.0-2.amzn2023.0.4.noarch`

Licenses (from `rpm --query`): MIT and (BSD or ASL 2.0)

Source:

```console
$ dnf --quiet download --source --url python3-setuptools-wheel-59.6.0-2.amzn2023.0.4.noarch
https://cdn.amazonlinux.com/al2023/core/guids/78a1f37d281a9c8eb5115c4f9b2f8306b103426d1c252c1a59e532225ea7a73b/SRPMS/../../../../blobstore/5a5f4927ec7c2bedc6a3c1e430840d97b19c6a4694ef75d67bcd51a6777b10da/python-setuptools-59.6.0-2.amzn2023.0.4.src.rpm
```

### `rpm` package: `readline-8.1-2.amzn2023.0.2.x86_64`

Licenses (from `rpm --query`): GPLv3+

Source:

```console
$ dnf --quiet download --source --url readline-8.1-2.amzn2023.0.2
https://cdn.amazonlinux.com/al2023/core/guids/78a1f37d281a9c8eb5115c4f9b2f8306b103426d1c252c1a59e532225ea7a73b/SRPMS/../../../../blobstore/236522110da6f9a9e2381da4a8a6b04625bebfcc6826497eea5838226c2f6ecb/readline-8.1-2.amzn2023.0.2.src.rpm
```

### `rpm` package: `rpm-4.16.1.3-29.amzn2023.0.6.x86_64`

Licenses (from `rpm --query`): GPLv2+

Source:

```console
$ dnf --quiet download --source --url rpm-4.16.1.3-29.amzn2023.0.6
https://cdn.amazonlinux.com/al2023/core/guids/78a1f37d281a9c8eb5115c4f9b2f8306b103426d1c252c1a59e532225ea7a73b/SRPMS/../../../../blobstore/2527ab9e1825bc6ad87e881431c9245a260dfaae70d820a8769dcb4f2cb38abc/rpm-4.16.1.3-29.amzn2023.0.6.src.rpm
```

### `rpm` package: `rpm-build-libs-4.16.1.3-29.amzn2023.0.6.x86_64`

Licenses (from `rpm --query`): GPLv2+ and LGPLv2+ with exceptions

Source:

```console
$ dnf --quiet download --source --url rpm-build-libs-4.16.1.3-29.amzn2023.0.6
https://cdn.amazonlinux.com/al2023/core/guids/78a1f37d281a9c8eb5115c4f9b2f8306b103426d1c252c1a59e532225ea7a73b/SRPMS/../../../../blobstore/2527ab9e1825bc6ad87e881431c9245a260dfaae70d820a8769dcb4f2cb38abc/rpm-4.16.1.3-29.amzn2023.0.6.src.rpm
```

### `rpm` package: `rpm-libs-4.16.1.3-29.amzn2023.0.6.x86_64`

Licenses (from `rpm --query`): GPLv2+ and LGPLv2+ with exceptions

Source:

```console
$ dnf --quiet download --source --url rpm-libs-4.16.1.3-29.amzn2023.0.6
https://cdn.amazonlinux.com/al2023/core/guids/78a1f37d281a9c8eb5115c4f9b2f8306b103426d1c252c1a59e532225ea7a73b/SRPMS/../../../../blobstore/2527ab9e1825bc6ad87e881431c9245a260dfaae70d820a8769dcb4f2cb38abc/rpm-4.16.1.3-29.amzn2023.0.6.src.rpm
```

### `rpm` package: `rpm-sign-libs-4.16.1.3-29.amzn2023.0.6.x86_64`

Licenses (from `rpm --query`): GPLv2+ and LGPLv2+ with exceptions

Source:

```console
$ dnf --quiet download --source --url rpm-sign-libs-4.16.1.3-29.amzn2023.0.6
https://cdn.amazonlinux.com/al2023/core/guids/78a1f37d281a9c8eb5115c4f9b2f8306b103426d1c252c1a59e532225ea7a73b/SRPMS/../../../../blobstore/2527ab9e1825bc6ad87e881431c9245a260dfaae70d820a8769dcb4f2cb38abc/rpm-4.16.1.3-29.amzn2023.0.6.src.rpm
```

### `rpm` package: `sed-4.8-7.amzn2023.0.2.x86_64`

Licenses (from `rpm --query`): GPLv3+

Source:

```console
$ dnf --quiet download --source --url sed-4.8-7.amzn2023.0.2
https://cdn.amazonlinux.com/al2023/core/guids/78a1f37d281a9c8eb5115c4f9b2f8306b103426d1c252c1a59e532225ea7a73b/SRPMS/../../../../blobstore/6984c7088347ffa40afb5e4e102396b0ae1a11af59e6afc04c1500e100521d7b/sed-4.8-7.amzn2023.0.2.src.rpm
```

### `rpm` package: `setup-2.13.7-3.amzn2023.0.2.noarch`

Licenses (from `rpm --query`): Public Domain

Source:

```console
$ dnf --quiet download --source --url setup-2.13.7-3.amzn2023.0.2.noarch
https://cdn.amazonlinux.com/al2023/core/guids/78a1f37d281a9c8eb5115c4f9b2f8306b103426d1c252c1a59e532225ea7a73b/SRPMS/../../../../blobstore/5039da404de01f584d0a4a717c5212948045a2d4feacadf42f4af1c8af7fdb3e/setup-2.13.7-3.amzn2023.0.2.src.rpm
```

### `rpm` package: `sqlite-libs-3.40.0-1.amzn2023.0.4.x86_64`

Licenses (from `rpm --query`): Public Domain

Source:

```console
$ dnf --quiet download --source --url sqlite-libs-3.40.0-1.amzn2023.0.4
https://cdn.amazonlinux.com/al2023/core/guids/78a1f37d281a9c8eb5115c4f9b2f8306b103426d1c252c1a59e532225ea7a73b/SRPMS/../../../../blobstore/dee50b94309acbd750702f8b6411e65f96d141d074b2c941a1b6239a0396eac2/sqlite-3.40.0-1.amzn2023.0.4.src.rpm
```

### `rpm` package: `system-release-2023.5.20240708-1.amzn2023.noarch`

Licenses (from `rpm --query`): MIT

Source:

```console
$ dnf --quiet download --source --url system-release-2023.5.20240708-1.amzn2023.noarch
https://cdn.amazonlinux.com/al2023/core/guids/78a1f37d281a9c8eb5115c4f9b2f8306b103426d1c252c1a59e532225ea7a73b/SRPMS/../../../../blobstore/61553bd93aa64dc68f6cac839342047d90b93541f26966889cbd8fb13ce9bb26/system-release-2023.5.20240708-1.amzn2023.src.rpm
```

### `rpm` package: `tar-1.34-1.amzn2023.0.4.x86_64`

Licenses (from `rpm --query`): GPLv3+

Source:

```console
$ dnf --quiet download --source --url tar-1.34-1.amzn2023.0.4
https://cdn.amazonlinux.com/al2023/core/guids/78a1f37d281a9c8eb5115c4f9b2f8306b103426d1c252c1a59e532225ea7a73b/SRPMS/../../../../blobstore/5a1f7da086290133e9d24d6eca3d019c9ef716a74f63576097d26661dc95baf2/tar-1.34-1.amzn2023.0.4.src.rpm
```

### `rpm` package: `tzdata-2024a-1.amzn2023.0.1.noarch`

Licenses (from `rpm --query`): Public Domain

Source:

```console
$ dnf --quiet download --source --url tzdata-2024a-1.amzn2023.0.1.noarch
https://cdn.amazonlinux.com/al2023/core/guids/78a1f37d281a9c8eb5115c4f9b2f8306b103426d1c252c1a59e532225ea7a73b/SRPMS/../../../../blobstore/56c8d3b2876a723a305c212f4924cd537ae791afe5100a4d397a0d42ea1b0089/tzdata-2024a-1.amzn2023.0.1.src.rpm
```

### `rpm` package: `which-2.21-26.amzn2023.0.2.x86_64`

Licenses (from `rpm --query`): GPLv3

Source:

```console
$ dnf --quiet download --source --url which-2.21-26.amzn2023.0.2
https://cdn.amazonlinux.com/al2023/core/guids/78a1f37d281a9c8eb5115c4f9b2f8306b103426d1c252c1a59e532225ea7a73b/SRPMS/../../../../blobstore/0ec4bfba149c3d82d3924d60802c4878107bb4b79fcfaff7a7ac7d1b1d4bbc1f/which-2.21-26.amzn2023.0.2.src.rpm
```

### `rpm` package: `xml-common-0.6.3-56.amzn2023.0.2.noarch`

Licenses (from `rpm --query`): GPL+

Source:

```console
$ dnf --quiet download --source --url xml-common-0.6.3-56.amzn2023.0.2.noarch
https://cdn.amazonlinux.com/al2023/core/guids/78a1f37d281a9c8eb5115c4f9b2f8306b103426d1c252c1a59e532225ea7a73b/SRPMS/../../../../blobstore/d8ae948bf9724a633a8cac71f26118e58f421263fe05ce13267c034e8e8f4c89/sgml-common-0.6.3-56.amzn2023.0.2.src.rpm
```

### `rpm` package: `xz-libs-5.2.5-9.amzn2023.0.2.x86_64`

Licenses (from `rpm --query`): Public Domain

Source:

```console
$ dnf --quiet download --source --url xz-libs-5.2.5-9.amzn2023.0.2
https://cdn.amazonlinux.com/al2023/core/guids/78a1f37d281a9c8eb5115c4f9b2f8306b103426d1c252c1a59e532225ea7a73b/SRPMS/../../../../blobstore/4d580fbb93e0ef7ee56606d496d780d5c80b9e2505ba176d44032dde2149b6ab/xz-5.2.5-9.amzn2023.0.2.src.rpm
```

### `rpm` package: `yum-4.14.0-1.amzn2023.0.5.noarch`

Licenses (from `rpm --query`): GPLv2+

Source:

```console
$ dnf --quiet download --source --url yum-4.14.0-1.amzn2023.0.5.noarch
https://cdn.amazonlinux.com/al2023/core/guids/78a1f37d281a9c8eb5115c4f9b2f8306b103426d1c252c1a59e532225ea7a73b/SRPMS/../../../../blobstore/3c7a286acf75f92e2600171b3b97237f9db9bf5b9466013b3c1686501ad6e7cd/dnf-4.14.0-1.amzn2023.0.5.src.rpm
```

### `rpm` package: `zlib-1.2.11-33.amzn2023.0.5.x86_64`

Licenses (from `rpm --query`): zlib and Boost

Source:

```console
$ dnf --quiet download --source --url zlib-1.2.11-33.amzn2023.0.5
https://cdn.amazonlinux.com/al2023/core/guids/78a1f37d281a9c8eb5115c4f9b2f8306b103426d1c252c1a59e532225ea7a73b/SRPMS/../../../../blobstore/a125f0c74adc4dcb176eec38955562d70c6ee7751ca7ec52156d74cbce9023d9/zlib-1.2.11-33.amzn2023.0.5.src.rpm
```

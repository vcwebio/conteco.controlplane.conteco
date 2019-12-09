##### BEGIN modeco.base/Dockerfile/image-header #####
FROM $CONTECO_REGISTRY$CONTECO_REALM/conteco.$CONTECO_BASE AS base
##### END modeco.base/Dockerfile/image-header #####

##### BEGIN modeco.base/Dockerfile/conteco #####
COPY ./modeco/ /modeco/
RUN rm -rf /conteco/repo
COPY ./ /conteco/repo/
##### END modeco.base/Dockerfile/conteco #####

##### BEGIN image/Dockerfile/build-instructions #####
##### END image/Dockerfile/build-instructions #####

##### BEGIN modeco.base/Dockerfile/env-labels-footer #####
ENV CONTECO_REALM="$CONTECO_REALM" \
    CONTECO_ECOSYSTEM="$CONTECO_ECOSYSTEM" \
    CONTECO_TYPE="$CONTECO_TYPE" \
    CONTECO_NAME="$CONTECO_NAME" \
    CONTECO_TAG="$CONTECO_TAG" \
    CONTECO_BASE="$CONTECO_BASE" \
    CONTECO_BUILD="$CONTECO_BUILD"
LABEL $CONTECO_LABELSPACE.schema-version="1.0" \
      $CONTECO_LABELSPACE.realm="$CONTECO_REALM" \
      $CONTECO_LABELSPACE.ecosystem="$CONTECO_ECOSYSTEM" \
      $CONTECO_LABELSPACE.type="$CONTECO_TYPE" \
      $CONTECO_LABELSPACE.name="$CONTECO_NAME" \
      $CONTECO_LABELSPACE.tag="$CONTECO_TAG" \
      $CONTECO_LABELSPACE.base="$CONTECO_BASE" \
      $CONTECO_LABELSPACE.build="$CONTECO_BUILD" \
      $CONTECO_LABELSPACE.label="$CONTECO_LABEL" \
      $CONTECO_LABELSPACE.description="$CONTECO_DESCRIPTION" \
      $CONTECO_LABELSPACE.docker.cmd.help="docker run ${CONTECO_REALM}/${CONTECO_ECOSYSTEM}.${CONTECO_TYPE}.${CONTECO_NAME} --help"
##### END modeco.base/Dockerfile/env-labels-footer #####

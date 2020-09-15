# Variant Data Model

<table>
  <thead>
    <tr>
      <th style="text-align:left">
        <p><b>id</b>
        </p>
        <p><em>String</em>
        </p>
      </th>
      <th style="text-align:left">Unique variant ID, this consists of chromosome, position, reference and
        alternate alleles in this format: <em>chrom:pos:ref:alt</em>
      </th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">
        <p><b>names</b>
        </p>
        <p><em>List&lt;String&gt;</em>
        </p>
      </td>
      <td style="text-align:left">Other IDs found for this genomic variant across all VCF files indexed</td>
    </tr>
    <tr>
      <td style="text-align:left">
        <p><b>chromosome</b>
        </p>
        <p><em>String</em>
        </p>
      </td>
      <td style="text-align:left">The chromosome where the genomic variant is located</td>
    </tr>
    <tr>
      <td style="text-align:left">
        <p><b>start</b>
        </p>
        <p><em>int</em>
        </p>
      </td>
      <td style="text-align:left">The 1-based position where the genomic variant starts. For variants coming
        from VCF files, this position is likely to be normalised, in this case,
        the original call in the file is stored in <em>studies.files.call</em> (see
        below)</td>
    </tr>
    <tr>
      <td style="text-align:left">
        <p><b>end</b>
        </p>
        <p><em>int</em>
        </p>
      </td>
      <td style="text-align:left">The 1-based position where the genomic variant ends. For variants coming
        from VCF files, this position is likely to be normalised, in this case,
        the original call in the file is stored in <em>studies.files.call</em> (see
        below)</td>
    </tr>
    <tr>
      <td style="text-align:left">
        <p><b>reference</b>
        </p>
        <p><em>String</em>
        </p>
      </td>
      <td style="text-align:left">Reference allele. For variants coming from VCF files, this position is
        likely to be normalised, in this case, the original call in the file is
        stored in <em>studies.files.call</em> (see below)</td>
    </tr>
    <tr>
      <td style="text-align:left">
        <p><b>alternate</b>
        </p>
        <p><em>String</em>
        </p>
      </td>
      <td style="text-align:left">Alternate allele. For variants coming from VCF files, this position is
        likely to be normalised, in this case, the original call in the file is
        stored in <em>studies.files.call</em> (see below)</td>
    </tr>
    <tr>
      <td style="text-align:left">
        <p><b>strand</b>
        </p>
        <p><em>String</em>
        </p>
      </td>
      <td style="text-align:left">Reference strand for this variant, by default all variants are represented
        in the positive strand</td>
    </tr>
    <tr>
      <td style="text-align:left">
        <p><b>length</b>
        </p>
        <p><em>int</em>
        </p>
      </td>
      <td style="text-align:left">Length of the genomic variation which depends on the variant type</td>
    </tr>
    <tr>
      <td style="text-align:left">
        <p><b>type</b>
        </p>
        <p><em>VariantType</em>
        </p>
      </td>
      <td style="text-align:left">Type of variant, the accepted types and Sequence Ontology (SO) terms are:</td>
    </tr>
    <tr>
      <td style="text-align:left">
        <p><b>sv</b>
        </p>
        <p><em>StructuralVariation</em>
        </p>
      </td>
      <td style="text-align:left">Specific information for Structural Variants</td>
    </tr>
    <tr>
      <td style="text-align:left">
        <p><b>studies</b>
        </p>
        <p><em>List&lt;StudyEntry&gt;</em>
        </p>
      </td>
      <td style="text-align:left">Information specific to each study the variant was read from, such as
        samples or statistics</td>
    </tr>
    <tr>
      <td style="text-align:left"><b>annotatio</b>
      </td>
      <td style="text-align:left">&lt;em&gt;&lt;/em&gt;</td>
    </tr>
  </tbody>
</table>


# Java Mapping

Load when DTO/entity mapping is non-trivial.

- Use direct code for small mappings; use MapStruct when generated mapping removes meaningful repetition.
- Keep business decisions out of mappers.
- Make renamed, nested, nullable, and collection mappings explicit.
- Review generated behavior and test transformations that alter meaning.
- Treat Lombok as a project choice; avoid generated equality, constructors, or mutability that obscure entity and contract semantics.
